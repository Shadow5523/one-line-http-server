#one-line-http-server

<html>
  <style type=""text/css"">
      <!--
  html{
    font-size: 20px;
  }
  table{
    width: 90%;
    padding: 0px 10px;
  }
  table td{
    background-color: #000000;
    color: #00ff00;
    font-size: 20px;
  }
  p{
    margin-bottom: 30px;
  }
  em{
    text-indent:2em;
  }
	-->
  </style>

  <b><p>～使用方法～</p></b>
  <table>
    <p>Linuxで動かす方法を紹介します。
      <br>あらかじめ、TCP/12345ポートの通信を許可してください。</p>
    <p>
      <li type="square">コンソールを開き以下を実行</li>
      <table>
	<td><p>[root@eva:one-line-http-server]$ python http.py</p></td>
      </table>
    </p>

    <p>
      <li type="square">別のコンソールを開き以下を実行</li>
      <table>
	<td><p>[root@eva:one-line-http-server]$ telnet 127.0.0.1 12345</p></td>
      </table>
    </p>

    <p>
      <li type="square">以下のような結果が帰ってくれば成功です</li>
      <table>
	<td>
	  <p>Trying 192.168.1.21...
	    <br>Connected to 192.168.1.21.
	    <br>Escape character is '^]'.
	    <br>HTTP/1.0 200 OK
	    <br>Content-Length: 20
	    <br>Content-Type: text/html
	    <br>
	    <br>&lt;html&gt;Hello world&lt;/html&gt;Connection closed by foreign host.
	  </p>
	</td>
      </table>
    </p>
  </table>
  </html>
