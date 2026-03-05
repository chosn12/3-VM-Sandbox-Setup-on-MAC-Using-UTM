## Potential Networking Issues using UTM on Mac

The networking issues I encountered using NAT (shared network) setting is in UTM. 
- No connection between VMs
- Unable to find ip addresses of VMs
- Unable to update drivers for VMs 

## Solution:

Make sure UTM is accessible through your firewall. 

**To do this:**
1. Click the **apple** in the upper left hand corner.
2. Select **System Settings**, then select **Network** on the left pane.
3. Next, select **Firewall**
4. Then, select **options**
5. Click the **plus** at the bottom and add **UTM**.
6. Click **Ok**

**It should look like this when it's added**

<img width="525" height="700" alt="Screen Shot 2026-03-03 at 16 37 56 PM" src="https://github.com/chosn12/3-VM-Sandbox-Setup-on-MAC-Using-UTM/blob/main/docs/UTM-Allowed.png" />

This should resolve all the above issues mentioned with the shared network setting in UTM for each VM.

__

## Potential Connection When Pinging Windows 11 VM

This connection issue I encounted trying to ping Windows 11 VM
- Unreachable

## Solution:

Allow ICMP traffic through the Windows 11 VM firewall.

**To do this:**
1. On the **taskbar**, click in the **search window** and type: **firewall.**
2. Double click **Windows Defender Firewall.**
3. Double click **Advance settings.**
4. Click **Inbound Rules** in the left pane.
5. Click **New Rule** in the right pane.
6. Select **Custom**, then click **Next.**
7. **All programs** should be selected, click **Next.**
8. On Protocol drop down menu, select **ICMPv4.**
9. Click **Next**.
10. Click **Next**, again.
11. **Allow the connection** should already be selected, click **Next.**
12. All choices should be selected, click **Next.**
13. Name the rule **ICMPv4 Allow**, or whatever you like.
14. Click **Finish**

This new rule should now appear in the **Inbound Rules** column.

<img width="525" height="700" alt="Screen Shot 2026-03-03 at 16 37 56 PM" src="" />

