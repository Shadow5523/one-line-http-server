# one-line-http-server

##使用方法
Linux(CentOS7.1)で検証しています。

1. TCP/12345ポートの通信を許可します。
  ```sh
  [root@eva:one-line-http-server]$ emacs /etc/sysconfig/iptables

  #以下の行を追記 (COMMIT行上)
  -A RH-Firewall-1-INPUT -p tcp -m state --state NEW -m tcp --dport 12345 -j ACCEPT
  ```


2. コンソールを開き以下を実行
  ```sh
  [root@eva:one-line-http-server]$ python http.py
  #今回使うファイルをあらかじめダウンロードしてください。
  ```
  

3. 別のコンソールを開き以下を実行
  ```sh
   [root@eva:one-line-http-server]$ telnet 127.0.0.1 12345
  ```
  

4. 以下のような結果が帰ってくれば成功です。
  ```sh
  Trying 192.168.1.21...
  Connected to 192.168.1.21.
  Escape character is '^]'.
  HTTP/1.0 200 OK
  Content-Length: 20
  Content-Type: text/html

  <html>Hello world</html>Connection closed by foreign host.
p>

  ```
  