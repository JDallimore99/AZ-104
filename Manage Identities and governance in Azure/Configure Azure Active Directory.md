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

# Select Azure Active Directory editions
Azure Active Directory comes in four editions: Free, Microsoft 365 Apps, Premium P1, and Premium P2. The Free edition is included with an Azure subscription. The Premium editions are available through a Microsoft Enterprise Agreement, the Open Volume License Program, and the Cloud Solution Providers program. Azure and Microsoft 365 subscribers can also buy Azure Active Directory Premium P1 and P2 online.
### Azure Active Directory Free
The Free edition provides user and group management, on-premises directory synchronization, and basic reports. Single sign-on access is supported across Azure, Microsoft 365, and many popular SaaS apps.

### Azure Active Directory Microsoft 365 Apps
This edition is included with Microsoft 365. In addition to the Free features, this edition provides Identity and Access Management for Microsoft 365 apps. The extra support includes branding, MFA, group access management, and self-service password reset for cloud users.

### Azure Active Directory Premium P1
In addition to the Free features, the Premium P1 edition lets your hybrid users access both on-premises and cloud resources. This edition supports advanced administration like dynamic groups, self-service group management, and cloud write-back capabilities. P1 also includes Microsoft Identity Manager, an on-premises identity and access management suite. The extra features in P1 allow self-service password reset for your on-premises users.

### Azure Active Directory Premium P2
In addition to the Free and P1 features, the Premium P2 edition offers Azure AD Identity Protection to help provide risk-based Conditional Access to your apps and critical company data. Privileged Identity Management is included to help discover, restrict, and monitor administrators and their access to resources, and to provide just-in-time access when needed.

# Implement Azure Active Directory join
Azure Active Directory enables single sign-on (SSO) to devices, applications, and services from anywhere. To support SSO, IT admins must ensure corporate assets are protected, and devices meet standards for security and compliance.
![image](https://user-images.githubusercontent.com/118181672/224962693-0ab91e1b-ea92-4176-8557-7ba56d571364.png)
The Azure AD join feature works with SSO to provide access to organizational apps and resources, and to simplify Windows deployments of work-owned devices.

Things to know about the Azure AD join feature
Let's look at some of the benefits of using joined devices:

|Benefit	|Description|
|:--|:---|
|Single-Sign-On (SSO)	|Joined devices offer SSO access to your Azure-managed SaaS apps and services. Your users won't have extra authentication prompts when they access work resources. The SSO functionality is available even when users aren't connected to the domain network.|
|Enterprise state roaming|	Starting in Windows 10, your users can securely synchronize their user settings and app settings data to joined devices. Enterprise state roaming reduces the time to configure a new device.|
|Access to Microsoft Store for Business	|When your users access Microsoft Store for Business by using an Azure AD account, they can choose from an inventory of applications pre-selected by your organization.|
|Windows Hello	|Provide your users with secure and convenient access to work resources from joined devices.|
|Restriction of access	|Restrict user access to apps from only joined devices that meet your compliance policies.|
|Seamless access to on-premises resources	|Joined devices have seamless access to on-premises resources, when the device has line of sight to the on-premises domain controller.|

Things to consider when using joined devices
Your organization is interested in using joined devices in their management strategy. As you plan for how to implement the feature, review these configuration points:

Consider connection options. Connect your device to Azure AD in one of two ways:
- Register your device to Azure AD so you can manage the device identity. Azure AD device registration provides the device with an identity that's used to authenticate the device when a user signs into Azure AD. You can use the identity to enable or disable the device.
- Join your device, which is an extension of registering a device. Joining provides the benefits of registering, and also changes the local state of the device. Changing the local state enables your users to sign into a device by using an organizational work or school account instead of a personal account.

Consider combining registration with other solutions. Combine registration with a mobile device management (MDM) solution like Microsoft Intune, to provide other device attributes in Azure AD. You can create conditional access rules that enforce access from devices to meet organization standards for security and compliance.

Consider other implementation scenarios. Although AD Join is intended for organizations that don't have an on-premises Windows Server Active Directory infrastructure, it can be used for other scenarios like branch offices.
