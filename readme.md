# Check NIST for CVEs with specific keywords  



To use:
```yaml
ansible-playbook main.yml  
```


---

## Excluded Files  
  - keys.yml  

```yaml
#### SLACK  
# token to message - Channel: #team-infosec    
slack_domain: "101101workspace.slack.com"
slack_channel: "#prom-integ"
slack_token: "XXXXXXXX/XXXXXXXX/XXXXXXXXXXXXXXXXXXXXXXXXXXX"

#### ServiceNOW  
SNOW_UID  : "xxxxxxxx"
SNOW_PWD  : "xxxxxxxxxxxxxxxxxx"

```  
---  

## VARs used in this playbook  
  - `BASE_URL`            - Root URL for the NIST API  
  - `SEVERITY`            - Severity of CVEs to pull  
  - `cve_pub_start_date`  - Today - 86400 seconds (24hrs ago)  
  - `cve_pub_start_time`  - Current time in UTC-05:00      
  - `cve_pub_end_date`    - Today  
  - `output`              - JSON payload returned from NIST  
  - `cve_id`              - CVE ID from NIST  
  - `cve_assigner`        - Who assigned the CVE  
  - `cve_pub_date`        - Date the CVE was published  
  - `cve_description`     - Description of the vulnerability  
  - `cve_severity`        - Severity  
  - `cve_attack_vector`   - How this CVE is exploited  
  - `KEYWORD`             - List of keywords to check against `output`  
  - `kwd_item`            - KEYWORD loop var  
  - `alert_created`       - Response from ServiceNOW  



    
---

![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73")  

