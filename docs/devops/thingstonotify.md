There are certain things that the DevOps team needs to know before or as they happen, generally to tweak some of talPor's support systems, be aware of the assets related to our projects, have a sense of the scope and importance of each project, be aware of possible security risk, etc. These are:

### Changes in the role of servers
**If a server changes roles (ie. From dev to production, production to dev, from main server to being db only, etc)**. Certain changes in the provisioning system need to be done so production servers can be handled with special care.

### New assets
**If any new asset (servers, dbs, accounts, mailgun, third party services, etc) are needed/created for the project**. This includes servers/services that the client obtained on their own, even if they are not under our control.
Understandably, the client might not inform us all the assets related to the project, and it is not our job to interrogate the client about the services that he/she contracts. But if knowledge of any machines relevant to the project reaches us (ie. a new server in AWS, a new business metrics solution, a new ftp server, etc), be sure to inform the operations team of the new asset and how it fits within the project structure.

### Server and service moves/Management changes
**If a server/service is moved or changed or management is given to a different team**. For example is the client decides to handle system administration on their own, or if they move the database to a dedicated server, or if they move the landing page to another server, or if the DNS or hosting is moved to a different provider. Contratation of new development teams that are not with talPor must also be notified.

### DNS record changes related to any server related to the project
**Any DNS record changes in the domain of the project or in a related and relevant domain (FQDN changes, new subdomains, DKIM, SPF, etc)**. For example, some clients rename the project several times at the beginning, wich sometimes results in domain name changes early on.

### Upcoming events
**Any events that require close awareness of the status of the server**. For example: marketing campaigns, exhibitions of the product, special dates that might attract high volumes of traffic and/or unwanted attention (ie. 9/11 on a site about the terrorist attacks of 9/11).

### Addition/Handling of sensitive information
**If the project handles or begins to handle sensitive data (addresses, names, emails, passwords, financial information, etc)** this fact must be reported to the operations team along with the nature and quantity of sensitive data stored.
Remember that most users repeat passwords across sites and that doxing and identity theft have been used with criminal purposes, so even seemingly innocuous information can be sensitive. Make sure to be on the safe side and push your client for TLS protection, we really don’t want to end up in https://haveibeenpwned.com.

### Changes in relationship with the client
**If the relations with the client become any other than normal or common**, for example unhappy clients where relations are getting difficult, client that miss a lot of payments, clients where talPor has a particularly high stake, etc.
In particular, instances where the relations with the client have formally stopped or are severely diminished must be reported.

### Projects where downtime is critical
**If downtime of the project could lead to serious consequences**. This specially important for projects that are enjoying success and to which any downtime could lead to significant financial losses, or for projects that are struggling and where any financial losses could prove disastrous.
It also applies to critical services (ie. medical systems) where downtime could lead to grave consequences and/or legal proceedings against talPor.

### Employee getting fired, specially if they are unhappy
**If, unfortunately, any employee of any department is fired or resigns from the company, either in good or bad terms**, this must be informed immediately to the operations team, so as to have his credentials revoked and email accounts suspended. This is especially critical if the break up of relations is not smooth.

### Employee mistakes
**If an employee makes an irreversible mistake that has or could have lead to serious consequences** (erasing an important database, forwarding a cryptolocker ransomware, leaking secret information about a client, using weak passwords for vital systems, etc) this should be informed to the operations team and the project manager.
The objective here is not to punish (though a reprimand might be necessary), but to make sure that the employee knows of his mistake, how to avoid it, and to adapt our protocols to avoid similar mistakes in the future.

### If in doubt, DO NOTIFY
**If in doubt about whether to notify the operations team, do notify**. That way we can determine if your concern is valid and evolve our protocol for notification of events to the operations team.

