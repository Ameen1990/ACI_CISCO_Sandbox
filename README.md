
# Coding_Challenge



Creating an ansible playbook that reads the following objects from the supplied variable file and


creates them in the Cisco Sandbox APIC:• Tenants, • Application profiles, • End point groups,  • Bridge domains,  • Contracts,  • VRFs,  etc.


The Cisco Sandbox APIC is an online testing environment hosted by Cisco.

Login data:

Hostname: https://sandboxapicdc.cisco.com/

User: admin

Password: !v3G@!4@Y




Ansible playbbok must read its specification from varaibles file "coding_challenge_ansible.yml"

Ansible must be installed locally.

Python3 is also a must.

Another Sandbox login solution is presented here:-

https://devnetsandbox.cisco.com/

log in with CISCo ID or Gmail account.

"Reservable ACI similator" was used where one can book it (max 6 hours) with total dedication to the user.

it's a recommended solution for testing purposes only , coz you will loose your configuration after the 6 hours limit.

Prerequsites: -

Download cisco AnyConnect VPN client from here: https://developer.cisco.com/site/sandbox/anyconnect/ or from Microsfot Store.

After clicking reserve, you will recieve two emails, the second one has the VPN credentials.

Once you logged in with VPN credentials, your APIC is availabe at: -

https://10.10.20.14

user: admin

pass: C1sco12345

Notes: -
- Those credentials are fixed for all reservable ACI simulators.
- Make sure that the switches (leaves and spine) are already there, if not, then add them manually.
- The process in triggered from "final.yml" Playbook.
- Screenshots are attached in Issues section.

If you get this error:-
ERROR ! couldnt resolve module/action 'cisco.aci.extepg_to_contrcat'  

Run the below command: -

"ansible-galaxy collection install cisco.aci"
