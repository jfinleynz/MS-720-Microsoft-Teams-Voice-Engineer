
---
lab:
    title: 'Lab: Manage your Teams Voice Environment'
    type: 'Answer Key'
    module: 'Module 1: Plan and configure Teams Phone'
---

# Lab 04: Manage your Teams Phone environment
# Student lab answer key

## Lab Scenario

Contoso need to make changes to existing users who are enabled for Teams Voice and add Teams Devices. Whilst making changes, support tickets have been raised due to problems users have reported with connectivity and troubleshooting must be performed.

## Lab Duration

  - **Estimated Time to complete**: 180 minutes

## Instructions

## Exercise 1: Manage voice users

### Exercise Duration

  - **Estimated Time to complete**: 30 minutes

In this exercise, you will perform day-to-day management tasks for Teams Voice users. 

### Task 1 - Change user call pickup settings

In this task you will sign into the Microsoft Teams Admin Center and make changes so that Isaiah’s colleague Katie can pick up their calls.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft Teams admin center** as **Katie Jordan**.

2. In the left navigation menu select **Users** and find **Isaiah Langer** and select the name to open the user’s properties.

3. On the user’s properties page, select the **Voice** tab.

4. Under the **Group call pickup** section, select **Add people**.

5. Search for **Katie Jordan** and select **Add** to include them in the **People list**, then select Apply.

6. As Katie would prefer an on-screen notification to show, rather than Teams to ring when Isaiah is unavailable, find **Katie Jordan** in the Group Call Pickup list. 

7. In the **Notification** column, update the value from **Ring** to **Banner** from the drop-down menu.

8. In the left navigation menu select **Users** to exit the properties page for Isaiah Langer.

The changes are now applied, and a banner will show for calls directed to Isaiah on Katie’s Teams client, allowing them to answer in the event that Isaiah is not able to.

### Task 3 - Configure call delegation

In this task you will configure Alex Wilber so that Katie Jordan is a delegate of Alex Wilber and is allowed to make calls on their behalf, but not receive calls.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft Teams admin center** as **Katie Jordan**.

2. Select **Users** and **Manage users**.

3. Find **Alex Wilber** and select the name to open the user’s properties.

4. On the user’s properties page, select the **Voice** tab.

5. Scroll down to **Call delegation** and select **Add people**

6. Search for **Katie Jordan**, and select **Add** to include them on the **People list**, then select **Apply.**

7. In the list below **Call delegation**, find **Katie Jordan** and Change the **Permission** value from **Make and receive calls** to **Make calls**. Switch the **Allow changing call settings** radio button to **Off**.

8. Leave the browser window open.

The changes are now active.

### Task 4 - Enable audio conferencing

In this task you validate audio conferencing is enabled for Katie Jordan and change the default settings.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft Teams admin center** as **Katie Jordan**.

2. Select **Users** and **Manage users**.

3. Find **Katie Jordan** and select the name to open the user’s properties.

4. On the user’s properties page, select the **Account** tab and under **Audio Conferencing** select **Edit.**

5. Check if **Audio Conferencing** is switched to **On.**

6. Set **Include toll-free numbers in meeting requests from user** to **Off**.

7. Select the **Toll number** dropdown and change it to **+1 689 206 9333 Orlando, United States**.

8. Select **Apply**.

9. Leave the browser window open.

You have successfully modified the audio-conferencing settings for Katie Jordan. 

### Task 5 - Assign a dial out policy

In this task you will assign a new Dial out policy to Megan Bowen, to restrict her from making outbound calls.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft Teams admin center** as **Katie Jordan**.

2. Select **Users** and **Manage users**.

3. Find **Megan Bowen** and select the name to open the user’s properties.

4. On the user’s properties page, select the **Voice** tab.

5. Under **Outbound calling**, select **Don’t allow** from the drop-down menu.

6. Wait until the notification **The dial out policy was assigned** shows, then select **Manage users** to exit the properties page.

7. Select the circle with the **KJ** initials in the upper right-side and select **Sign out**.

8. Close the browser window open for the end of this task.

Outbound calls from Megan Bowen have been restricted.

## Exercise 2: Manage Teams devices

### Exercise Duration

  - **Estimated Time to complete**: 30 minutes

In this exercise we will watch a demonstration video to show the end-to-end process for provisioning a Teams IP Phone. We will then create and license an account to use with a Microsoft Teams Room system.

### Task 1 - Perform remote provisioning of Teams Phones

In the demonstration video, we gather information required to perform remote provisioning of a Teams IP Phone at Contoso’s Bellevue location.

On the Teams Phone, we then enter provisioning information to ensure it is ready to be signed in by a user and can be managed by our organization. The following steps are performed.

1. Open Microsoft Edge from the task bar and browse to the **Microsoft Teams admin center** at [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com/).

2. Sign in as **Katie Jorden**, who has the Teams Administrator role.

3. Select **Devices** and then select **IP Phones**.

4. Select **Actions in the upper right corner**, then from the drop-down menu, select **Provision Devices.**

5. The **Provision devices** page shows. Under **Waiting on activation** select **Add MAC addresses manually**.

6. In the **Add MAC** addresses dialogue, enter the MAC address and location, Bellevue, for the Teams IP Phone.

7. Select **Apply** to save the change.

8. The **Waiting on activation page** will show the Teams IP Phone’s MAC address and location. Select the MAC address from the list, then select **Generate verification code**

9. On the Teams IP Phone, select **Settings,** then choose **Provision phone**

10. Enter the generated verification code on the Teams IP Phone, then select **Next**

11. **Device provisioned successfully** should display on the Teams IP Phone screen.

12. In the Teams Admin Center, on the **Provision devices** page, choose **Refresh**, then choose the **Waiting for sign in** tab. The Teams IP Phone will show in the list.

13. Select the circle in the upper right-side with the **KJ** initials and select Sign out.

14. Close the browser window at the end of this task.

The Teams IP Phone can now be signed in to by a user or remotely signed in to a common area account.

### Task 2 - Create license and enable Enterprise Voice for a Microsoft Teams Room account 

In this task, we will create and license a Microsoft Teams Room device account using Windows PowerShell. This will be for the Contoso Board Room at the Bellevue site and use Direct Routing for voice calls.

1. You are still signed in to CLIENT01 as “Lab User”.

2. Open Microsoft Edge from the task bar and browse to the Microsoft 365 admin center at [https://admin.microsoft.com](https://admin.microsoft.com/).

3. Sign in as the **MOD Administrator** with the credentials provided.

4. Select **Billing** then choose **Purchase Services**.

5. Search for **Microsoft Teams Room Standard** from the list of available services and select **Details**.

6. Select **Start free trial,** then on the following page, choose **Try now.**

7. Download the SkypeRoomProvisioning.ps1 script from the Microsoft website: [https://go.microsoft.com/fwlink/?linkid=870105](https://go.microsoft.com/fwlink/?linkid=870105)

8. Open File Explorer and navigate to the **Downloads** folder and open **SkypeRoomProvisioningScript.ps1.txt.**

9. Launch a Windows PowerShell command prompt as an Administrative user.

10. Change directory to a location suitable for creating a script, and then create a new file named SkypeRoomProvisioningScript.ps1 by entering the following command.

    ```console
    cd $HOME\Documents
    
    notepad .\SkypeRoomProvisioningScript.ps1
    ```

11. When prompted **Do you want to create a new file?** select **Yes**

12. In the Notepad Window for SkypeRoomProvisioningScript.ps1.txt, copy all text using **CTRL-A** and then **CTRL-C.**

13. In the Notepad Window for SkypeRoomProvisioningScript.ps1, use **CTRL-V** to paste the PowerShell script from the clipboard, and then select **File** then select **Save**.

14. Make sure you have the latest MSOnline PowerShell module installed with the following cmdlet. If you receive an **Untrusted repository** prompt, select **Yes to all**.

    ```powershell
    Update-Module MSOnline
    ```

15. Make sure you have the latest Exchange Online PowerShell modules installed with the following cmdlet. If you receive an **Untrusted repository** prompt, select **Yes to all**.

    ```powershell
    Update-Module ExchangeOnlineManagement
    ```

16. Run the script with the following command:

    ```powershell
    .\SkypeRoomProvisioningScript.ps1
    ```

17. From the script menu choice, enter **2** for a Skype Room Systems v2 device, and then press Enter.

18. Enter **1** to create the account in AD, Exchange and Skype, and then press Enter.

19. Enter **2** to create the account in the cloud, then press Enter.

20. Enter **2** when asked if your users are synced to Office 365, then press Enter.

21. A Windows PowerShell credential request window appears. Enter the credentials of your **MOD Administrator**.

22. A Windows PowerShell credential request window appears, asking you the **Enter the desired UPN and password for this new room account**. Enter mtr01@\<labnumber\>.onmicrosoft.com and enter a secure password you will remember.

23. Enter the following display name for the account and then press Enter.

    - **Bellevue Board Room**

24. The next menu in the PowerShell script will provide a list of available licenses. Select the **MEETING_ROOM SKU**

25. To provision the Exchange Room mailbox, choose **2** to provision the user in the cloud, then press Enter.

26. Enter **2** when asked to confirm if the Exchange Online admin account is different from the Global Administrator account, then press Enter. The process will take approximately 10 minutes to complete.

27. The script will state that the mailbox has been created. An opportunity to automatically configure the calendar processing defaults, so that Automatic Calendar Processing is enabled will be presented. Enter **1** for Yes, then press Enter.

28. When prompted to provision Skype, enter **2** for in the cloud, then press **Enter**.

29. Enter **2** when asked to confirm if the Skype for Business Online admin account is different from the Global Administrator account, then press Enter.

30. The account will now be enabled for Microsoft Teams (based upon the tenant being in **Teams Only Mode**) and the script will attempt to set up the account as a meeting room. This may take approximately 5 minutes.

31. When prompted to configure **Enterprise Voice** for the room, choose **1** for Yes, then press Enter.

32. Enter the following E.164 number for the room, without a **tel:+** prefix: 14255551123 

33. Check the LineURI stated is correct and shows as tel:+14255551123 and then choose **1** to accept, then press Enter.

34. Close the PowerShell Window at the end of the task.

Upon completion of the script a summary of actions will be stated, including a statement that the script has **Successfully configured a room mailbox for the account**. The account can now be signed-in to a Microsoft Teams Room system using the password provided in step **21**.

### Task 3 - Prepare to manage devices by creating tags in the Teams Admin Center

In this task you will configure device tags to allow Contoso to identify devices based upon the type of employee that will use the device, so that the importance of the device can be identified by a support technician. We will configure two tags, **Executive** and **Contact Center**.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft 365 admin center** as **MOD Administrator**.

2. Navigate to the Microsoft Teams admin center at [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com/).

3. Select **Teams devices**, then select **Phones.**

4. Select **Actions**, then from the upper right-side and select **All Device tags**.

5. From the **Manage tags** dialogue, select **Add**.

6. Enter **Executive** and choose the **Save** icon.

7. Select **Add**.

8. Enter **Contact Center** and select the **Save** icon.

9. Select **Cancel** to close the Manage Tags dialogue.

10. Leave the browser window open for the next task.

As devices are provisioned or joined, they will be displayed in the **Devices** section of the Teams Admin Center. Although no devices are available during the lab exercise, you will expect after a device is added that you can then assign the tags to a device, by selecting the **Device** in the list and then selecting **Manage Tags**, then searching for a tag, and selecting **Apply.**

After applying a tag to devices, you can then use the **Search** box in the device list to choose **Select what you want to search by**, and then choosing **Tags**. Enter the tag you’ve assigned to devices, and these devices will be displayed in the search results.

## Exercise 3: Monitor and troubleshoot Teams Phone

### Exercise Duration

  - **Estimated Time to complete**: 120 minutes

In this exercise, you will perform exercises to help troubleshoot specific issues and monitor call use and quality.

### Task 1 - Run self-help diagnostics tool in Microsoft 365 admin center

Megan Bowen has reported they are not receiving voicemails. Microsoft offers some Self-help diagnostics tools that can be run before raising a support ticket. In this task you will run the Voicemail diagnostic that validates that a user is properly configured to use Voicemail in Teams.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft 365 admin center** as **MOD Administrator**.

2. Navigate to the **Microsoft 365 admin center** at admin.microsoft.com.

3. On the left menu, select **Show all**, then **Users** and **Active Users.** 

4. Find Megan Bowen and note down their username and email address, you will need it to run the test. Note this is one value in the format MeganB@\<TenantPrefix\>.onmicrosoft.com

5. On the left menu, select **show all**, then **Support** and under the support menu **New service request.**

6. In the **Tell us about the problem so we can help you solve it** dialogue, enter **Diag: Voicemail** and press enter to jump straight to the voicemail diagnostics test.

7. You will see the following diagnostics test **We understand you are having issues with receiving voicemails in Teams.** Under Username or Email enter Megan Bowen’s Username and email.

8. Select **Run Tests.**

9. The result should be **No Teams Voicemail issues were detected.**

You have successfully used the Microsoft 365 self-help diagnostics to confirm that there are no configuration issues with Megan Bowen’s voicemail.

### Task 2 - Break a dial plan and check the issue

In this lab we are going to create and then break a dial plan rule and check Call Analytics to see the issue.

Firstly, we will create a dial plan rule, in this scenario, the organization would like the short code 7786 to translate to +1-877-696-7786.

1. You are still signed in to CLIENT01 as “Lab User” and signed into the **Microsoft 365 admin center** as **MOD Administrator**.

2. Navigate to the **Microsoft Teams admin center** at [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com/).

3. Select **Voice** and **Dial Plan**.

1. Select the **Global (org wide default)** dial plan.

2. Under Normalization rules select **Add** to get to the add new rule dialogue.

3. For **Name** enter **Converts 7786 to US support number**.

4. For **Description** enter **Converts 7786 to US support number**.

5. Ensure **Basic** rule is selected, it should be by default.

6. Tick **The number dialed begins with** and enter 7.

7. Tick **The length of the number being dialed is** and enter 4.

8. Ensure **Exactly** is selected for length of number to be dialed.

9. Tick **Add this number to the beginning** and enter +1877696.

10. Test the rule by entering **7786** and pressing Test. The output should be **+18776967786**, if the output is correct select **Save**.

11. You will see your new rule in the global dial plan, select **Save.**

12. Close the browser window.

You have successfully added a normalization rule to a dial plan to meet the extension dialing organizational requirement.

We will now confirm the rule works with a real user

1. You are still signed into CLIENT01 as “Lab User” from the previous task.

2. From the desktop select and run Microsoft Teams client.

3. You should still be signed in as Megan Bowen on the Teams Desktop client. If not, sign in using the credentials of Megan Bowen.

4. You will be prompted with **Stay signed into all your apps** select **No, sign in to this app only.**

5. If you are prompted with the Teams welcome information:

	- **Bring your team together,** select **Next.**

	- Chat 1:1 and with groups, select **Next.**

	- Connect through online meetings, select **Next.**

	- Files, notes, apps, and more, all in one place, select **Next.**

	- You're ready!, select **Let’s go.**

6. **I**f you are prompted **Get the Teams mobile app**, select the top right **X** to close the prompt.

7. Select the calls button on the left rail.

8. Dial **7786** and press call.

9. If your lab machine prompted you to use your microphone select **Allow.**

10. If you are prompted by Windows Defender Firewall for Microsoft Teams select **Allow Access.**

11. Note that the number has been translated to +18776967786 and the call connects. It is an contact center that will stay connected for around a minute then automatically hang up.

12. Press the red hang-up button to disconnect the call.

Now we have proven the rule works, we will break the rule and confirm the rule.

1. You are still signed into CLIENT01 as “Lab User” from the previous task.

2. Sign out of Microsoft Teams Desktop client, select the **MB** account icon and **Sign out.**

3. Open Microsoft Edge from the task bar and browse to the Microsoft Teams admin center at [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com/).

4. Select **Voice** and **Dial Plan**. 

5. Select the **Global (org wide default)** dial plan.

6. Select the **Converts 7786 to US support number** rule to edit it.

7. Note it will be converted to an advanced regular expression now.

8. In the field the number dialed matches this regular expression, it will read ^(7\d{3})$

9. Replace the 7 with a 6 to now read, ^(6\d{3})$ 

10. Test the rule by entering 7786 and pressing Test. The output should be the translated number isn't an E.164 phone number.

11. Select **Save**.

12. At the dial plan page, again select **Save** to update the global dial plan.

Now we have broken our dial plan, we will sign into Teams again and prove it is no longer working

1. You are still signed into CLIENT01 as “Lab User” from the previous task.

2. From the desktop select and run Microsoft Teams client.

3. Select Get started.

4. When prompted for sign in, enter Alex Wilber’s username and select **Next.**

5. When prompted enter Alex Wilber’s password and select **Next.**

6. You will be prompted with “Stay signed into all your apps” select **No, sign in to this app only.**

7. If you are prompted with the Teams welcome information.

	- **Bring your team together,** select **Next.**

	- Chat 1:1 and with groups, select **Next.**

	- Connect through online meetings, select **Next.**

	- Files, notes, apps, and more, all in one place, select **Next.**

	- You're ready!, select **Let’s go.**

8. Once signed in, Select the calls button on the left rail.

9. Dial 7786 and press call.

10. If your lab machine prompted you to use your microphone select **Allow.**

11. If you are prompted by Windows Defender Firewall for Microsoft Teams select **Allow Access.**

12. Note that Teams attempts to ring the number but it does not connect or you get the Teams. Announcement Service telling you the call cannot connect.

13. Press the red hang-up button to disconnect the call.

You have successfully created a dial plan, proven it works, broken it and seen the user impact of a broken dial plan.

### Task 3 - Review Call Health Real Time Stats on a live call

Users can check on the network performance of their calls live during the call. In this task we will test the Team call health feature

1. You are still signed into CLIENT01 as “Lab User” from the previous task

2. From the desktop select and run **Microsoft Teams** client

3. You should still be signed in as **Alex Wilber**.

4. Select the calls button on the left rail.

5. Dial +1-877-696-7786 and press call.

6. If your lab machine prompted you to use your microphone select **allow.**

7. If you are prompted by Windows Defender Firewall for Microsoft Teams select **Allow Access.**

8. The call should establish and you should hear a Microsoft support virtual agent.

9. While in the call, press the three dots in the top right of the Teams client and select call health.

10. You will see a right-hand menu with the network and audio performance.

Call Health shows you the following:

#### Network Metrics

| Metric| Description |
|:---------|:---------|
| Roundtrip time| In group calls, it's the response time between your system and the Teams Service. In one-on-one calls, it's the response time between your system and the other participant's. Lower is better. |
| Received packet loss| In group calls, it's the response time between your system and the Teams Service. In one-on-one calls, it's the response time between your system and the other participant's. Lower is better. |
| Teams send limit| The max limit of data Teams can send based on the current network conditions and how it's used. This isn't your ISP speed limit. |
| Teams send limit| The max limit of data Teams can receive based on the current network conditions and how it's used. This isn't your ISP speed limit. |

#### Audio

| Metric| Description |
|:---------|:---------|
| Sent bitrate| The amount of audio data sent. High is better. |
| Sent packets| Data gets sent over the network in packets. This value is the number of data packets sent during a call. |
| Roundtrip time| Response time between your system and the Teams server. Lower is better. |
| Sent codec| The codec used for encoding audio sent by your system. |
| Received jitter| The distortion in audio caused by inconsistent audio packet arrival times. Lower is better |
| Received packets| The number of audio data packets received |
| Received packet loss| The result of a poor network connection, this is the percentage of audio data packets not received by your system. Lower is better |
| Received codec| The codec used for encoding audio data received by your system. |


### Task 4 - Use the Microsoft 365 connectivity test tool

A Teams Phone user working from home reports they are having call quality issues, we will use the Microsoft 365 connectivity test tool to check they are tasking an optimum network path to Office 365 and check their basic Teams network performance

1. Sign into CLIENT01 as “Lab User” with the password provided to you. In this task we will treat Client01 as the PC of the user with the problem.

2. Open Microsoft Edge from the task bar and browse to [https://connectivity.office.com/](https://connectivity.office.com/).

3. Ensure **Automatically detect location** is selected and select **Run test.**

4. Microsoft Edge may prompt you that connectivity.office.com wants to know your location, if it does, select **Allow.**

5. The browser will prompt you to Open or Save as a new download, select **open** and Office 365 Network Onboarding Advanced Tests box will appear and start running tests.

6. You will get a prompt to install .Net Core, would you like to download it now, click Yes

7. This will take you to the .net core download site, Under Run desktop apps select Download

8. When the download is complete, select open file

9. The Microsoft Windows Desktop Runtime installer will appear, click Install

10. A UAC prompt will appear, click Yes

11. Once the .net core installer is complete, click close

12. Close Microsoft Edge

13. Open Microsoft Edge and browse to [https://connectivity.office.com/](https://connectivity.office.com/).

14. Ensure **Automatically detect location** is selected and select **Run test.**

15. Microsoft Edge may prompt you that connectivity.office.com wants to know your location, if it does, select **Allow.**

16. The browser will prompt you to Open or Save as a new download, select **open** and Office 365 Network Onboarding Advanced Tests box will appear and start running tests.

17. You will see a green progress bar and “testing in progress”, wait for all tests to complete. You maybe prompted with Windows Defender Firewall prompts from NetworkOnboardingClient – select **Allow Access.**

18. Once the Office 365 Network Onboarding Advanced Tests box says testing is complete, select **Close.**

19. Microsoft Edge should still be open, you can now see a summary of the results

20. Select Details and scroll down to review the following:

	- Exchange service front door location and SharePoint Online front door locations should have green ticks.

	- Under Microsoft Teams look for green ticks for connectivity, packet loss, latency and jitter.

If the user does not have green ticks for Microsoft teams network performance, check to see if they are using WiFi or can wire directly into their router to confirm if it is an ISP issue or local network/WiFi issue.

If they front door locations do not have green ticks and they are not using any VPN we may need to contact their local ISP for support. 

You have successfully tested network connectivity and performance from a user’s machine using the Microsoft 365 network test tool.

### Task 5 - Inspect PSTN Usage Reports

The Teams PSTN (Public Switched Telephone Network) usage report in the Microsoft Teams admin center gives you an overview of calling and audio conferencing activity in your organization. 

In this task we will review the PSTN Usage report.

1. You are still signed into CLIENT01 as “Lab User” from the previous task.

2. Open Microsoft Edge from the task bar and browse to the **Microsoft Teams admin center** at [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com/).

3. You should be singed in as **MOD Administrator**.

4. Select **Analytics &amp; reports** on the left menu then **Usage reports.**

5. Under report select the **PSTN and SMS (preview) usage** report.

6. Under Date range select **last 7 days.**

7. Select **Run report.**

You will see a report showing all the PSTN calls made in the last 7 days. You should see the test calls we made with Alex Wilber in this exercise. Note, it may take some time for the call records to show. 

The report shows:

- **Time stamp (UTC)** is the time the call started.

- **Display name** is the display name of the user. You can click the display name to go to the user's setting page in the Microsoft Teams admin center.

- **Username** is the user's sign in name.

- **Phone number** is the number that received the call for inbound calls or the number dialed for outbound calls.

- **Call type** is whether the call was a PSTN outbound or inbound call and the type of call such as a call placed by a user or an audio conference. 

- **Called to** is the number dialed.

- **To country or region** is the country or region dialed.

- **Called from** is the number that placed the call.

- **From country or region** is the country or region from where the call was placed.

- **Charge** is the amount of money or cost of the call that's charged to your account.

- **Currency** is the type of currency used to calculate the cost of the call.

- **Duration** is how long the call was connected.

- **Domestic/International** tells you whether the call was domestic (within a country or region) or international (outside a country or region) based on the user's location.

- **Call ID** is the call ID for a call. It's an identifier for the call you can use when calling Microsoft Support.

- **Number type** is the user's phone number type, such as a service of toll-free number.

- **Country or region** is the usage location.

- **Conference ID** is the conference ID of the audio conference.

- **Capability** is the license used for the call.

You have successfully generated and reviewed the PSTN usage report

### Task 6 - Review Calls in Call Analytics

If we want to review the usage and performance of an individuals Teams calling, the first place to look is Call Analytics in the Teams Admin Center. In this task we will review Alex Wilber’s calls in Call Analytics

1. You are still signed into CLIENT01 as “Lab User” and in the **Microsoft Teams admin center** as **MOD Administrator**.

2. Select **Users** and **Manage users** on the left menu.

3. Find and select **Alex Wilber.**

4. Select the **Meetings &amp; calls** tab.

5. You can now see all recent calls and meetings made by or involving Alex. Note, you may need to scroll down.

6. Select one of the longer calls by duration.

7. In the top bar, note how teams rated the overall Audio quality.

You can see device, system, connectivity and network information. Note that since we are running tests from a virtual machine information will not be complete, for example device information may not be populated.

8. In the **Overview** tab Select **Network** and review the network metrics.

9. Select the **Advanced** tab to see all key metrics on one page.

10. Select the **Debug** tab to see all metrics (complete and incomplete).

You now know how to access and review call and meeting information in Call Analytics in the Teams Admin Center.

### Task 7 - Review Calls in Call Quality Dashboard

A Voice Administrator should look at the call and meeting usage and performance across the entire environment. This can be done by reviewing the Microsoft Call Quality Dashboard

In this task you open and review Call Quality Dashboard

1. You are still signed into CLIENT01 as “Lab User” and in the **Microsoft Teams admin center** as **MOD Administrator**.

2. At the bottom of the left menu, select **Call Quality Dashboard**.

3. This will cause a new browser tab to open going to [https://cqd.teams.microsoft.com/](https://cqd.teams.microsoft.com/).

4. You will need to again login as a Tenant Administrator, select **Sign In** top right.

5. You should be automatically signed in, if not, provide your Tenant Administrator credentials.

As we have not made many calls in this environment, and when making calls in lab virtual machine not all metrics are provided to the Teams service, some reports will be blank and incomplete.

6. As an example, select **Help Desk Reports** from the top menu and on the Help Desk report page select the **Call Details** tab to see recent calls.

In this task you have learnt how to open and navigate Call Quality Dashboard.
