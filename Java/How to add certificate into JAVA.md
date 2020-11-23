How to add certificate into JAVA

1. to get the certificate from the website. You would get the .cer file.

2. the default location of the trustStore is at %JAVA_HOME%/jre/lib/security such as C://Program Files/Java/jdk1.8.0_221/jre/lib/security/cacerts

3. use the command(keytool -importcert) to put the certificate into your keystore such as the following command:
	<code>
		keytool -importcert -trustcacerts -alias "cert_name" -file "/tmp/cert_name.cer" -keystore "%JAVA_HOME%/jre/lib/security" -storepass "changeit"
	</code>
	
4. After completing step 3, we can use JAVA to send a request to the untrust website equipping the self-sign certificate

