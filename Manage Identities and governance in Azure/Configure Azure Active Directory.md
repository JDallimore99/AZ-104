# Describe Azure Active Directory benefits and features
Azure Active Directory (Azure AD) is Microsoft's multi-tenant cloud-based directory and identity management service. Azure AD helps to support user access to resources and applications, such as:
- Internal resources and apps located on your corporate network.
- External resources like Microsoft 365, the Azure portal, and SaaS applications.
- Cloud apps developed for your organization.

## Azure AD Features

|Azure AD feature	|Description|
|:---|:---|
|Single sign-on (SSO) access|	Azure AD provides secure single sign-on (SSO) to web apps on the cloud and to on-premises apps. Users can sign in with the same set of credentials to access all their apps.|
|Ubiquitous device support	|Azure AD works with iOS, macOS, Android, and Windows devices, and offers a common experience across the devices. Users can launch apps from a personalized web-based access panel, mobile app, Microsoft 365, or custom company portals by using their existing work credentials.|
|Secure remote access|	Azure AD enables secure remote access for on-premises web apps. Secure access can include multifactor authentication (MFA), conditional access policies, and group-based access management. Users can access on-premises web apps from everywhere, including from the same portal.|
|Cloud extensibility|	Azure AD can extend to the cloud to help you manage a consistent set of users, groups, passwords, and devices across environments.|
|Sensitive data protection	|Azure AD offers unique identity protection capabilities to secure your sensitive data and apps. Admins can monitor for suspicious sign-in activity and potential vulnerabilities in a consolidated view of users and resources in the directory.|
|Self-service support|	Azure AD lets you delegate tasks to company employees that might otherwise be completed by admins with higher access privileges. Providing self-service app access and password management through verification steps can reduce helpdesk calls and enhance security.|

# Describe Azure Active Directory concepts 

|Azure AD concept|	Description|
|:---|:---|
|Identity|	An identity is an object that can be authenticated. The identity can be a user with a username and password. Identities can also be applications or other servers that require authentication by using secret keys or certificates. Azure AD is the underlying product that provides the identity service.|
|Account	|An account is an identity that has data associated with it. To have an account, you must first have a valid identity. You can't have an account without an identity.|
|Azure AD account	|An Azure AD account is an identity that's created through Azure AD or another Microsoft cloud service, such as Microsoft 365. Identities are stored in Azure AD and are accessible to your organization's cloud service subscriptions. The Azure AD account is also called a work or school account.|
|Azure tenant (directory)|	An Azure tenant is a single dedicated and trusted instance of Azure AD. Each tenant (also called a directory) represents a single organization. When your organization signs up for a Microsoft cloud service subscription, a new tenant is automatically created. Because each tenant is a dedicated and trusted instance of Azure AD, you can create multiple tenants or instances.|
|Azure subscription	|An Azure subscription is used to pay for Azure cloud services. Each subscription is joined to a single tenant. You can have multiple subscriptions.|

# Compare Active Directory Domain Services to Azure Active Directory
Active Directory Domain Services (AD DS) is the traditional deployment of Windows Server-based Active Directory on a physical or virtual server. AD DS is commonly considered to be primarily a directory service, but it's only one component of the Windows Active Directory suite of technologies.
The following characteristics that distinguish Azure AD from AD DS:
- Identity solution: AD DS is primarily a directory service, while Azure AD is a full identity solution. Azure AD is designed for internet-based applications that use HTTP and HTTPS communications. The features and capabilities of Azure AD support target strong identity management.
- REST API queries: Azure AD is based on HTTP and HTTPS protocols. Azure AD tenants can't be queried by using LDAP. Azure AD uses the REST API over HTTP and HTTPS.
- Communication protocols: Because Azure AD is based on HTTP and HTTPS, it doesn't use Kerberos authentication. Azure AD implements HTTP and HTTPS protocols, such as SAML, WS-Federation, and OpenID Connect for authentication (and OAuth for authorization).
- Federation services: Azure AD includes federation services, and many third-party services like Facebook.
- Flat structure: Azure AD users and groups are created in a flat structure. There are no organizational units (OUs) or group policy objects (GPOs).
- Managed service: Azure AD is a managed service. You manage only users, groups, and policies. If you deploy AD DS with virtual machines by using Azure, you manage many other tasks, including deployment, configuration, virtual machines, patching, and other backend processes.

