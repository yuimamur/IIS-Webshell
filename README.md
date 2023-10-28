# IIS-Webshell

# Windows ServerでIIS インストール

サーバマネージャを起動する。

![image](https://github.com/yuimamur/IIS-Webshell/assets/59761194/7e5b9b4f-ada4-4776-aed6-15878d9a347b)

「役割と機能の追加(Add Roles and Features)」を選択します。

![image](https://github.com/yuimamur/IIS-Webshell/assets/59761194/a1f9f786-9055-4af1-bf28-61c7bdb51919)

サーバーの役割(Server Roles) の選択画面で「Webサーバー（IIS）」を選択するようにします。

<img width="775" alt="image" src="https://github.com/yuimamur/IIS-Webshell/assets/59761194/438b6cff-3b77-45d0-9240-6959342389fb">

<img width="775" alt="image" src="https://github.com/yuimamur/IIS-Webshell/assets/59761194/5d9e90c6-144c-4bd8-a945-9d1c8789d424">

# インストール確認

インストール完了後、IIS Managerを立ち上げる。

<img width="535" alt="image" src="https://github.com/yuimamur/IIS-Webshell/assets/59761194/0304e121-88e9-4cb9-8c41-ce6056b0ceeb">

Browse Website から Browse *.80 (http) をクリックする。
もしくは、ブラウザを立ち上げて「http://localhost/iisstart.htm」にアクセスします。

Explorer を立ち上げて、C:\inetpub\wwwroot へアクセスする。

sample.aspx として保存する。Encoding を Unicode とする。
```
<%@ Page Language="C#" %>
<script runat="server">
protected void Page_Load(Object source, EventArgs e) {
    MyLabel.Text = "日本語でこんちちは！";
}
</script>
<HTML>
<BODY>
    <asp:Label runat="server" id="MyLabel" />
</BODY>
</HTML>
```

# Web Shell の設置

下記からファイルをダウンロードし、同様のフォルダに配置する。

https://github.com/yuimamur/yuimamur-tools/raw/main/cmdasp.aspx
<br> Command からコマンドを実行する。

<img width="752" alt="image" src="https://github.com/yuimamur/IIS-Webshell/assets/59761194/a850f5fe-e869-41ec-a36b-2dd77d9a287f">

