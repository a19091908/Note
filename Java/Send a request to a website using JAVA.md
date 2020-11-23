Send a request to a website using JAVA

the JAVA code is in the following:

<code>	
String urlStr = "https://cardt.tcbt.com/ECS";
URL url = new URL(urlStr);	
HttpURLConnection urlConnection = (HttpURLConnection) url.openConnection();
urlConnection.setRequestMethod("POST");

// urlConnection.connect(); // this line is not necessary because the command urlConnection.getInputStream() or urlConnection.getOutputStream() would invoke urlConnection.connect() automatically
if (urlConnection.getResponseCode()==HttpURLConnection.HTTP_OK) {
	// get the response body for the request
	try(BufferedInputStream bis = new BufferedInputStream(urlConnection.getInputStream())){
		byte[] by = new byte[1024];
		while(bis.read(by) != -1) {
			System.out.print(new String(by ,"utf-8"));
		}
	}
}else {
	System.out.println("ERROR");
}
</code>
		