---
title: 'Tutorial: Azure Active Directory integration with PurelyHR | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and PurelyHR.
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman

ms.assetid: 86a9c454-596d-4902-829a-fe126708f739
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 04/20/2017
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with PurelyHR

In this tutorial, you learn how to integrate PurelyHR with Azure Active Directory (Azure AD).

Integrating PurelyHR with Azure AD provides you with the following benefits:

- You can control in Azure AD who has access to PurelyHR
- You can enable your users to automatically get signed-on to PurelyHR (Single Sign-On) with their Azure AD accounts
- You can manage your accounts in one central location - the Azure portal

If you want to know more details about SaaS app integration with Azure AD, see [what is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).

## Prerequisites

To configure Azure AD integration with PurelyHR, you need the following items:

- An Azure AD subscription
- A PurelyHR single-sign on enabled subscription

> [!NOTE]
> To test the steps in this tutorial, we do not recommend using a production environment.

To test the steps in this tutorial, you should follow these recommendations:

- Do not use your production environment, unless it is necessary.
- If you don't have an Azure AD trial environment, you can get a one-month trial [here](https://azure.microsoft.com/pricing/free-trial/).

## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding PurelyHR from the gallery
2. Configuring and testing Azure AD single sign-on

## Adding PurelyHR from the gallery
To configure the integration of PurelyHR into Azure AD, you need to add PurelyHR from the gallery to your list of managed SaaS apps.

**To add PurelyHR from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon. 

	![Active Directory][1]

2. Navigate to **Enterprise applications**. Then go to **All applications**.

	![Applications][2]
	
3. To add new application, click **New application** button on the top of dialog.

	![Applications][3]

4. In the search box, type **PurelyHR**.

	![Creating an Azure AD test user](./media/purelyhr-tutorial/tutorial_purelyhr_search.png)

5. In the results panel, select **PurelyHR**, and then click **Add** button to add the application.

	![Creating an Azure AD test user](./media/purelyhr-tutorial/tutorial_purelyhr_addfromgallery.png)

##  Configuring and testing Azure AD single sign-on
In this section, you configure and test Azure AD single sign-on with PurelyHR based on a test user called "Britta Simon."

For single sign-on to work, Azure AD needs to know what the counterpart user in PurelyHR is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in PurelyHR needs to be established.

In PurelyHR, assign the value of the **user name** in Azure AD as the value of the **Username** to establish the link relationship.

To configure and test Azure AD single sign-on with PurelyHR, you need to complete the following building blocks:

1. **[Configuring Azure AD Single Sign-On](#configuring-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Creating an Azure AD test user](#creating-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
3. **[Creating a PurelyHR test user](#creating-a-purelyhr-test-user)** - to have a counterpart of Britta Simon in PurelyHR that is linked to the Azure AD representation of user.
4. **[Assigning the Azure AD test user](#assigning-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Testing Single Sign-On](#testing-single-sign-on)** - to verify whether the configuration works.

### Configuring Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal and configure single sign-on in your PurelyHR application.

**To configure Azure AD single sign-on with PurelyHR, perform the following steps:**

1. In the Azure portal, on the **PurelyHR** application integration page, click **Single sign-on**.

	![Configure Single Sign-On][4]

2. On the **Single sign-on** dialog, select **Mode** as	**SAML-based Sign-on** to enable single sign-on.
 
	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_purelyhr_samlbase.png)

3. On the **PurelyHR Domain and URLs** section, perform the following steps if you wish to configure the application in **IDP** initiated mode:

	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_purelyhr_url.png)
   
	In the **Reply URL** textbox, type a URL using the following pattern: `https://<companyID>.purelyhr.com/sso-consume`

4. Check **Show advanced URL settings**, if you wish to configure the application in **SP** initiated mode:

	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_purelyhr_url1.png)
    
	In the **Sign-on URL** textbox, type the value using the following pattern: `https://<companyID>.purelyhr.com/sso-initiate`
	 
	> [!NOTE]
	> These values are not the real. Update these values with the actual Reply URL and Sign-On URL. Contact [PurelyHR Client support team](http://support.purelyhr.com/) to get these values. 

5. On the **SAML Signing Certificate** section, click **Certificate (Base64)** and then save the certificate file on your computer.

	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_purelyhr_certificate.png) 

6. Click **Save** button.

	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_general_400.png)
	
7. On the **PurelyHR Configuration** section, click **Configure PurelyHR** to open **Configure sign-on** window. Copy the **SAML Entity ID and SAML Single Sign-On Service URL** from the **Quick Reference section.**

	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_purelyhr_configure.png) 

8. To configure single sign-on on **PurelyHR** side, login to their website as an administrator.

9. Open the **Dashboard** from the options in the toolbar and click **SSO Settings**.

10. Paste the values in the boxes as described below-

	![Configure Single Sign-On](./media/purelyhr-tutorial/purelyhr-dashboard-sso-settings.png)	

	a. Open the **Certificate(Bas64)** downloaded from the Azure portal in notepad and copy the certificate value. Paste the copied value into the **X.509 Certificate** box.

	b. In the **Idp Issuer URL** box, paste the **SAML Entity ID** copied from the Azure portal.

	c. In the **Idp Endpoint URL** box, paste the **SAML Single Sign-On Service URL** copied from the Azure portal. 

	d. Check the **Auto-Create Users** checkbox to enable automatic user provisioning in PurelyHR.

	e. Click **Save Changes** to save the settings.

> [!TIP]
> You can now read a concise version of these instructions inside the [Azure portal](https://portal.azure.com), while you are setting up the app!  After adding this app from the **Active Directory > Enterprise Applications** section, simply click the **Single Sign-On** tab and access the embedded documentation through the **Configuration** section at the bottom. You can read more about the embedded documentation feature here: [Azure AD embedded documentation]( https://go.microsoft.com/fwlink/?linkid=845985)
> 

### Creating an Azure AD test user
The objective of this section is to create a test user in the Azure portal called Britta Simon.

![Create Azure AD User][100]

**To create a test user in Azure AD, perform the following steps:**

1. In the **Azure portal**, on the left navigation pane, click **Azure Active Directory** icon.

	![Creating an Azure AD test user](./media/purelyhr-tutorial/create_aaduser_01.png) 

2. To display the list of users, go to **Users and groups** and click **All users**.
	
	![Creating an Azure AD test user](./media/purelyhr-tutorial/create_aaduser_02.png) 

3. To open the **User** dialog, click **Add** on the top of the dialog.
 
	![Creating an Azure AD test user](./media/purelyhr-tutorial/create_aaduser_03.png) 

4. On the **User** dialog page, perform the following steps:
 
	![Creating an Azure AD test user](./media/purelyhr-tutorial/create_aaduser_04.png) 

    a. In the **Name** textbox, type **BrittaSimon**.

    b. In the **User name** textbox, type the **email address** of BrittaSimon.

	c. Select **Show Password** and write down the value of the **Password**.

    d. Click **Create**.
 
### Creating a PurelyHR test user

To enable Azure AD users to log in to PurelyHR, they must be provisioned into PurelyHR. In PurelyHR, provisioning is an automatic task and no manual steps are required when automatic user provisioning is enabled.

### Assigning the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to PurelyHR.

![Assign User][200] 

**To assign Britta Simon to PurelyHR, perform the following steps:**

1. In the Azure portal, open the applications view, and then navigate to the directory view and go to **Enterprise applications** then click **All applications**.

	![Assign User][201] 

2. In the applications list, select **PurelyHR**.

	![Configure Single Sign-On](./media/purelyhr-tutorial/tutorial_purelyhr_app.png) 

3. In the menu on the left, click **Users and groups**.

	![Assign User][202] 

4. Click **Add** button. Then select **Users and groups** on **Add Assignment** dialog.

	![Assign User][203]

5. On **Users and groups** dialog, select **Britta Simon** in the Users list.

6. Click **Select** button on **Users and groups** dialog.

7. Click **Assign** button on **Add Assignment** dialog.
	
### Testing single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

Click the Absorb LMS tile in the Access Panel, you get automatically signed-on to your Absorb LMS application.

For more information about the Access Panel, see. [Introduction to the Access Panel](https://msdn.microsoft.com/library/dn308586).

## Additional resources

* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)



<!--Image references-->

[1]: ./media/purelyhr-tutorial/tutorial_general_01.png
[2]: ./media/purelyhr-tutorial/tutorial_general_02.png
[3]: ./media/purelyhr-tutorial/tutorial_general_03.png
[4]: ./media/purelyhr-tutorial/tutorial_general_04.png

[100]: ./media/purelyhr-tutorial/tutorial_general_100.png

[200]: ./media/purelyhr-tutorial/tutorial_general_200.png
[201]: ./media/purelyhr-tutorial/tutorial_general_201.png
[202]: ./media/purelyhr-tutorial/tutorial_general_202.png
[203]: ./media/purelyhr-tutorial/tutorial_general_203.png

