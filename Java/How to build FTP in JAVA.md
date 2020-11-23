How to build FTP in JAVA

We use Socket to create a connection between local and remote server, 
and use input and out stram to download and upload data.

1. use Socket to connect the remote server

<code>
	FTPClient ftp = new FTPClient();
	FTPClientConfig config = new FTPClientConfig();
    config.setXXX(YYY); // change required options
    // for example config.setServerTimeZoneId("Pacific/Pitcairn")
    ftp.configure(config );
    String server = "ftp.example.com";
    ftp.connect(server);
</code>

2. check the reply code to verify success.

<code>
	reply = ftp.getReplyCode();

	if(!FTPReply.isPositiveCompletion(reply)) {
        ftp.disconnect();
        System.err.println("FTP server refused connection.");
        System.exit(1);
    }
</code>

3. change remote working folder to your desired folder path  
<code>
	boolean chgFolderResult = client.changeWorkingDirectory(remotrTargetFolderPath);
	if (!chgFolderResult)
        return false;
</code>
       

4. list all files in this remote path
<code>
	FTPFile[] files = client.listFiles();
    if (files != null && files.length > 0) {
        for (FTPFile file : files) {
          if (!file.isFile()) {
            continue;
          }
          boolean chkResult = checkFileName(file);
          if(chkResult){
            // download the file
          }
        }
    }
</code>

5. download/upload the file

(1) download
<code>
	boolean rst;

    try (FileOutputStream out = new FileOutputStream(sPLocalFileName);) {
      
      rst = ftp.retrieveFile(sPRemoteFileName, out); // download the file

      addFtpFileName(sPLocalFileName);

    } finally {
    }
    return rst;
</code>

(2) upload
<code>
	boolean rst;
    
    try (FileInputStream in = new FileInputStream(sPLocalFilePath);) {

      rst = client.storeFile(sPRemotePath, in);

      addFtpFileName(sPLocalFilePath);

    } finally {
    }
    return rst;
</code>

6. 

