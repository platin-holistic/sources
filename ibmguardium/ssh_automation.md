<h1>How to?</h1>

1. At machine you initialize IBM Guardium SSH automation;
    - Run <code>ssh-keygen</code> command.
         - Keep passphrase empty. (hit enter)
         - Overwrite if it asks.
           <img width="930" height="600" alt="image" src="https://github.com/user-attachments/assets/e133696b-dbba-4095-a612-189eb409a172" />

2. At machine you ran generate command;
    - Run <code>cat ~/.ssh/id_rsa.pub</code> command.
      <img width="1895" height="155" alt="image" src="https://github.com/user-attachments/assets/11ddfa07-7834-4c46-add6-a5a2d9a428a0" />

3. Copy all output and store it anywhere for pasting.

4. Access to Guardium CLI:
    - Run <code>store system public key authorized</code> command.
    - Paste public key you stored previous step.
      <img width="1126" height="376" alt="image" src="https://github.com/user-attachments/assets/cb3eea19-b7c9-40cd-b7ac-dab36b33959e" />
5. Now you can run commands via SSH access.

<h1>Examples</h1>
<b>You can run commands with printf by implementing to SSH.</b>

-  <code>printf 'support clean dam_data policy_violations 2025-01-01 2025-11-16\nconfirm delete' | ssh cli@<gdp_appliance_ip></code>
-  <code>printf 'support show db-top-tables all' | ssh cli@<gdp_appliance_ip></code>


