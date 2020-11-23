how to use https in localhost

1. create keystore:
	(1) use following command to produce .keystore file.
		"$JAVA_HOME\bin\keytool" -genkey -alias tomcat -keyalg RSA
	(2) the path of the file would display in the command line.

2. modify server.xml of tomcat (the version of tomcat is 9.0)
	(1) uncomment and modify some parts of the following string:
		<code>
			<Connector port="443" protocol="org.apache.coyote.http11.Http11NioProtocol"
    	           maxThreads="150" SSLEnabled="true" scheme="https">
    	    	<SSLHostConfig>
    	        	<Certificate certificateKeystoreFile="C:\Users\swu53\.keystore"
    	                         certificateKeystorePassword="changeit"
    	                         certificateKeyAlias="tomcat"
    	                         type="RSA" />
    	    	</SSLHostConfig>
    		</Connector>
		</code>
		(a) certificateKeystoreFile: the path of the keystore
		(b) certificateKeystorePassword: the password of the keystore
		(c) certificateKeyAlias: the alias of the key
		
