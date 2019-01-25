# sm Mail Send Modular
sm(Simple Mail)即简单邮件，它是基于python3中的smtplib模块进行的二次开发，功能跟smtplib没什么区别，但是其将繁琐的信息封装过程变得简单化。

## SimpleMail类 ##
> SimpleMail(...)
    SimpleMail(smtp_server,port=25,protocol='SMTP') -> SimpleMail Object

    smtp_server = SMTP server address, such as 163 smtp@163.com.
    port = SMTP service port number, if the protocol is SSL, use 465, customizable port number.
    protocol = Is the protocol used SMTP or SSL.

> SimpleMail(...)
    SimpleMail(smtp_server,port=25,protocol='SMTP') -> SimpleMail Object

    smtp_server = SMTP服务器地址，如163的smtp@163.com。
    port = SMTP服务端口号，如果协议是SSL，使用465，可自定义端口号。
    protocol = 是使用SMTP或SSL的协议。

## Login Function ##
> login(...)
    sm.login(send_user,send_pass) -> None

    Used to login to SMTP server.
    send_user = Mail User.
    send_pass = Mail Password.

## 登录函数 ##
> login(...)
    sm.login(send_user,send_pass) -> None

    用于登录到SMTP服务器。
    send_user = 邮件用户。
    send_pass = 邮件密码。

## Message Funtion ##
> message(...)
    sm.message_attach(sender,rect,subject='SimpleMail',content='SimpleMail Mail sent',subtype='plain',level=1) -> str

    Generate a mail message.
    sender = A tuple composed of the sender's name and the sender's address.
    rect = A list consisting of a recipient or multiple recipients and levels.
    subject = Mail subject.
    content = Mail content.
    subtype = Mail Type is plain or html.
    level = When the level is 2, it is sent at regular intervals. When the level is 3, it is sent by copy and sent at 3.

    Level needs to be used in conjunction with rect. When level is not 1, the list value of rect should be two.

## 生成邮件消息函数 ##
> message(...)
    sm.message(sender,rect,subject='SimpleMail',content='SimpleMail Mail sent',subtype='plain',level=1) -> str

    生成邮件消息。
    sender = 由发送者的姓名和发送者的地址组成的元组。
    rect = 由收件人或多个收件人和级别组成的列表。
    subject = 邮件主题。
    content = 邮件内容。
    subtype = 邮件类型是plain还是html的。
    level = 当级别为2时，它以抄送发送邮件。当级别为3时，它以密送发送邮件。

    level需要与rect一起使用。当级别不是1时，rect的列表值应该是两个。

## Message Attach Function ##
> message_attach(...)
    sm.message_attach(sender,rect,attach,subject='SimpleMail',content='SimpleMail Mail sent',subtype='plain',level=1) -> str

    Generate a mail message, including attachments.
    sender = A tuple composed of the sender's name and the sender's address.
    rect = A list consisting of a recipient or multiple recipients and levels.
    attach = A list or tuple consisting of one or more attachments.
    subject = Mail subject.
    content = Mail content.
    subtype = Mail Type is plain or html.
    level = When the level is 2, it is sent at regular intervals. When the level is 3, it is sent by copy and sent at 3.

    Level needs to be used in conjunction with rect. When level is not 1, the list value of rect should be two.

## 生成带附件的邮件消息函数 ##
> message_attach(...)
    sm.message_attach(sender,rect,attach,subject='SimpleMail',content='SimpleMail Mail sent',subtype='plain',level=1) -> str

    生成邮件消息，包括附件。
    sender = 由发送者的姓名和发送者的地址组成的元组。
    rect = 由收件人或多个收件人和级别组成的列表。
    attach = 由一个或多个附件组成的列表或元组。
    subject = 邮件主题。
    content = 邮件内容。
    subtype = 邮件类型是plain还是html的。
    level = 当级别为2时，它以抄送发送邮件。当级别为3时，它以密送发送邮件。

    level需要与rect一起使用。当级别不是1时，rect的列表值应该是两个。

## Send Mail Function ##
> sendmail(...)
    sm.sendmail(send_mail, rect_mail, message) -> bool

    If the message is sent successfully, it will return to true, otherwise it will return to false.
    send_mail = Email Sender.
    rect_mail = The recipient of a message represents one or more recipients in the form of a list.
    message = sm.message or sm.message_attach.

## 发送邮件函数 ##
> sendmail(...)
    sm.sendmail(send_mail, rect_mail, message) -> bool

    如果消息发送成功，它将返回true，否则它将返回false。
    send_mail = 电子邮件发送者。
    rect_mail = 消息的接收者以列表的形式表示一个或多个收件人。
    message = sm.message 或 sm.message_attach。
