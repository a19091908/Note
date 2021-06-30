<h2>FTPS</h2>

<h3>Explicit and Implicit Mode</h3>
1. Explicit Mode
    * The connection is kept protected during connecting.
    * Use port 990 as a listener for the control channel
    * Use port 989 as a listener for the data channel 
2. Implicit Mode
    * First, the connection is builded with plain text.
    * Then, the connection begins to be protected after the FTPS server receives the AUTH TLS by the FTPS client. 

<h3>Transfer data in a secured way</h3>
* Protect control channel
    - To protect the control channel, the AUTH command must be sent. So that the client and the server can communicate with each other on the control channel.
* Protect data channel
    - To protect the data channel, the PBSZ command, followed by the PROT command sequence, must be used.

<h3>Data Connection Security</h3>
1. PBSZ (protection buffer size) command
    - A data channel encapsulation mechanism for protected data buffers
    - For FTPS, the PBSZ command must still be issued, but must
      have a parameter of '0' to indicate that no buffering is taking
      place and the data connection should not be encapsulated.
2. PORT command
    - For TLS, the data connection can have one of two security levels.
        1. Clear (requested by 'PROT C')
            - Neither Integrity nor Privacy
            - The data connection is made without TLS
        2. Private (requested by 'PROT P')
            - Integrity and Privacy
            - The data connection is made with TLS

<h3>Reference</h3>
<div>
    <a href="https://datatracker.ietf.org/doc/html/rfc4217">Securing FTP with TLS</a>
</div>
<div>
    <a href="https://datatracker.ietf.org/doc/html/rfc2228">FTP Security Extensions</a>
</div>




