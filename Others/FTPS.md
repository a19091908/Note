<h2>FTPS</h2>

<h3>Explicit and Implicit Mode</h3>
1. Explicit Mode
    * The connection is kept protected during connecting.
    * Use port 990 as a listener for the control channel
    * Use port 989 as a listener for the data channel 
2. Implicit Mode
    * First, the connection is builded with plain text.
    * Then, the connection begins to be protected after the FTPS server receives the AUTH TLS by the FTPS client. 