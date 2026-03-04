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
