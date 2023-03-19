pipeline {
    agent any

    stages {
        stage('Send welcome email') {
            steps {
                script {
                    // Set the email configuration
                    def emailConfig = [
                        to: "kalex7878@gmail.com",
                        subject: 'Welcome to the system',
                        body: "Welcome to the system! Your username is alex_k and your password is 1234.",
                        mimeType: 'text/html',
                        replyTo: 'alufdavid@example.com',
                        cc: '',
                        bcc: '',
                        attachmentsPattern: '',
                        presendScript: '',
                        attachLog: false,
                        compressLog: false,
                        replyToAddress: '',
                        saveOutput: false,
                        messagePerCheckin: false,
                        numberOfLogLines: '',
                        maxAttachmentSize: '',
                        importance: 'normal',
                        priority: 'normal',
                        charset: 'UTF-8'
                    ]
                    
                    // Set the SMTP server configuration
                    def smtpServer = [
                        smtpHost: 'smtp.gmail.com',
                        smtpPort: '465',
                        smtpAuth: 'login',
                        smtpUser: 'alufdavid@gmail.com',
                        smtpPassword: 'smtp_token',
                        ssl: true,
                        starttls: true,
                        enableSslVerification: true,
                        smtpProtocol: 'smtp'
                    ]

                    // Send the email using the configured settings
                    mail to: emailConfig.to,
                         subject: emailConfig.subject,
                         body: emailConfig.body,
                         mimeType: emailConfig.mimeType,
                         replyTo: emailConfig.replyTo,
                         cc: emailConfig.cc,
                         bcc: emailConfig.bcc,
                         attachmentsPattern: emailConfig.attachmentsPattern,
                         presendScript: emailConfig.presendScript,
                         attachLog: emailConfig.attachLog,
                         compressLog: emailConfig.compressLog,
                         replyToAddress: emailConfig.replyToAddress,
                         saveOutput: emailConfig.saveOutput,
                         messagePerCheckin: emailConfig.messagePerCheckin,
                         numberOfLogLines: emailConfig.numberOfLogLines,
                         maxAttachmentSize: emailConfig.maxAttachmentSize,
                         importance: emailConfig.importance,
                         priority: emailConfig.priority,
                         charset: emailConfig.charset,
                         smtp: smtpServer
                }
            }
        }
    }
}
