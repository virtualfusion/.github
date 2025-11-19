---
name: VirtualFusion Incident Report Template
about: This template is used to record incidents that impact the VirtualFusion platform,
  track resolution progress, document root causes, and define preventive actions.
title: ''
labels: ''
assignees: ''

---

### **Incident Metadata**

| Field                  | Value                                                 |
| ---------------------- | ----------------------------------------------------- |
| **Incident ID**        | INC-YYYY-MM-DD-XXX                                    |
| **Severity**           | P0 (Critical), P1 (High), P2 (Medium), P3 (Low)       |
| **Status**             | Investigating, Identified, Monitoring, Resolved       |
| **Incident Commander** | @username                                             |
| **Start Time**         | YYYY-MM-DD HH:MM:SS                                   |
| **Detection Time**     | YYYY-MM-DD HH:MM:SS                                   |
| **Resolution Time**    | YYYY-MM-DD HH:MM:SS (or Ongoing)                      |
| **Duration**           | X hours Y minutes                                     |
| **Affected Services**  | Service1, Service2, Service3                          |
| **Customer Impact**    | Yes or No, number of affected customers or percentage |

---

### **1. Incident Summary**

#### **1.1 Executive Summary**

Provide a 2 to 3 sentence summary describing what happened, impact, and resolution status.

Example:
Primary PostgreSQL database experienced catastrophic failure at 14:32, resulting in complete data loss for tenant configurations. All customer-facing services were unavailable for 2.5 hours. System restored from backup with four-hour data loss window.

#### **1.2 Business Impact**

* **Service Availability:** X percent downtime
* **Affected Customers:** Number or percentage
* **Revenue Impact:** Estimated USD X (if calculable)
* **SLA Breach:** Yes or No, details
* **Reputation Risk:** High, Medium, Low

---

### **2. Technical Details**

#### **2.1 Affected Components**

**Service Layer**
[ ] API Gateway
[ ] Load Balancer
[ ] Backend Services

**Database Layer**
[ ] PostgreSQL
[ ] Redis
[ ] MongoDB

**Infrastructure**
[ ] Compute
[ ] Storage
[ ] Network

**Application**
[ ] Collector
[ ] Parser
[ ] AI Engine
[ ] RCA Module

#### **2.2 Root Cause (Initial Assessment)**

Provide detailed explanation of what caused the incident.

#### **2.3 Error Messages and Logs**

Paste relevant log excerpts, stack traces, error messages.

#### **2.4 System State at Time of Incident**

* **Database:** Type, version, host config
* **Records Before:** Count
* **Records After:** Count
* **Last Backup:** Timestamp
* **Storage Utilization:** Percentage
* **Active Connections:** Count or maximum

---

### **3. Incident Timeline**

#### **3.1 Detailed Chronology**

| Time (UTC) | Event                 | Action Taken                   | Owner  |
| ---------- | --------------------- | ------------------------------ | ------ |
| 14:30:00   | Incident detected     | Initial assessment started     | @user1 |
| 14:35:00   | Severity assessed     | Incident Commander assigned    | @user2 |
| 14:45:00   | Root cause identified | Mitigation plan initiated      | @user3 |
| 15:20:00   | Fix deployed          | Service restoration began      | @user4 |
| 16:00:00   | Service verified      | Monitoring activated           | @user5 |
| 17:00:00   | Incident resolved     | Post-incident review scheduled | @user1 |

#### **3.2 Detection Method**

[ ] Automated Monitoring Alert
[ ] Customer Report
[ ] Internal User Discovery
[ ] Multiple (specify)

---

### **4. Impact Analysis**

#### **4.1 Service Impact Matrix**

| Service        | Impact Level | Availability | Recovery Time |
| -------------- | ------------ | ------------ | ------------- |
| Collector API  | Critical     | 0 percent    | 2.5 hours     |
| Parser Agents  | Critical     | 0 percent    | 2.5 hours     |
| Dashboard UI   | High         | Read-only    | 2.5 hours     |
| RCA Engine     | High         | Failed       | 2.8 hours     |
| Reporting      | Medium       | Cached data  | 2.5 hours     |
| Authentication | None         | Unaffected   | N/A           |

#### **4.2 Data Impact**

* **Data Loss:** Yes or No
* **Scope:** Description
* **Criticality:** Critical, High, Medium, Low
* **Recovery:** Status
* **Manual Intervention Needed:** Yes or No, details

---

### **5. Resolution Steps**

#### **5.1 Immediate Actions (Mitigation)**

* Identified scope of issue
* Stopped automated processes
* Disabled affected services
* Initiated backup restoration
* Validated data integrity
* Restarted services
* Verified critical workflows

#### **5.2 Temporary Workarounds**

List temporary mitigation steps here.

---

### **6. Root Cause Analysis (RCA)**

#### **6.1 Five Whys Analysis**

1. Why did the incident occur?
2. Why did that happen?
3. Why did that occur?
4. Why was that the case?
5. Why did that condition exist?
   **Final answer should be the root cause.**

#### **6.2 Contributing Factors**

* Factor 1
* Factor 2
* Factor 3

#### **6.3 Was This Preventable?**

Explain prevention possibilities.

---

### **7. Action Items and Preventive Measures**

#### **7.1 Immediate Actions (Within 24 Hours)**

| Action Item                          | Owner   | Due Date |
| ------------------------------------ | ------- | -------- |
| Audit all automated maintenance jobs | @owner1 | Nov 15   |
| Implement backup validation checks   | @owner2 | Nov 15   |
| Add monitoring for row count changes | @owner3 | Nov 15   |

#### **7.2 Short-Term Actions (Within 1 Week)**

| Action Item                                 | Owner   | Due Date |
| ------------------------------------------- | ------- | -------- |
| Implement dry-run for delete operations     | @owner1 | Nov 21   |
| Create maintenance script testing framework | @owner2 | Nov 21   |
| Implement point-in-time recovery            | @owner3 | Nov 21   |

#### **7.3 Medium-Term Actions (Within 1 Month)**

| Action Item                                 | Owner   | Due Date |
| ------------------------------------------- | ------- | -------- |
| Implement database change approval workflow | @owner1 | Dec 14   |
| Conduct incident response training          | @owner2 | Dec 14   |
| Create disaster recovery runbook            | @owner3 | Dec 14   |

---

### **8. Post-Incident Review**

#### **8.1 What Went Well**

* Item 1
* Item 2
* Item 3

#### **8.2 What Needs Improvement**

* Item 1
* Item 2
* Item 3

#### **8.3 Lessons Learned**

* Lesson 1
* Lesson 2
* Lesson 3

#### **8.4 Incident Review Meeting**

* **Scheduled:** Date and time
* **Duration:** Duration
* **Attendees:** List names

---

### **9. External References**

#### **9.1 Related Tickets**

* Primary Ticket: ID
* Follow-up Tickets: List
* Customer Tickets: List
* Related Past Incidents: List

#### **9.2 Documentation**

* Runbook: URL
* Backup Procedures: URL
* Incident Response Playbook: URL

---

### **10. Severity Classification Guide**

| Severity        | Description                                                      | Response SLA | Resolution SLA |
| --------------- | ---------------------------------------------------------------- | ------------ | -------------- |
| **P0 Critical** | Complete outage, data loss, security breach, high revenue impact | 15 minutes   | 4 hours        |
| **P1 High**     | Major degradation or multiple customer complaints                | 30 minutes   | 24 hours       |
| **P2 Medium**   | Minor degradation or isolated customer impact                    | 4 hours      | 72 hours       |
| **P3 Low**      | Cosmetic or non-critical                                         | 24 hours     | 1 week         |

---

### **Attachments**

* Screenshots
* Log files (last 24 hours)
* Query execution plan
* Monitoring dashboard
* Network topology diagram
* Database schema diagram
* Backup restoration logs
* Customer communication screenshots

---

### **Approval**

* **Incident Commander:** @username
* **Signature:**
* **Date Closed:** YYYY-MM-DD HH:MM UTC
* **Final Status:** Resolved / Monitored / Closed
