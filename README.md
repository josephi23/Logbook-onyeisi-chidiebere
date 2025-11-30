# Logbook
## Date Started: 09.11.2025
**Author: Onyeisi Chidiebere**
This logbook records my progress and time spent on the Cybersecurity course assignments.

## Log Entries
| Date | Start Time | End Time | Hours Spent | Topic(s) | Output |
|------------|------------|----------|-------------|-----------------------------------------------|------------------------------------------------------------------------|
| 2025-11-09 | 09:30 | 10:00 | 0.5 hrs | Git repository setup | Created and initialized repo with README |
| 2025-11-09 | 10:00 | 10:30 | 0.5 hrs | Logbook creation | Added table format and first entries |
| 2025-11-09 | 11:00 | 12:00 | 1.0 hrs | Introduction to Cyber Security | Reviewed course materials and PortSwigger intro |
| 2025-11-10 | 14:00 | 15:30 | 1.5 hrs | SQL Injection (Lab 1) | "SQL injection vulnerability in WHERE clause allowing retrieval of hidden data" – watched YouTube for basic payload, got it with ' OR 1=1-- |
| 2025-11-10 | 20:00 | 20:40 | 0.7 hrs | SQL Injection (Lab 2) | "SQL injection vulnerability allowing login bypass" – logged in as administrator with administrator'-- |
| 2025-11-13 | 15:30 | 17:00 | 1.5 hrs | Authentication (Lab 1) | "Username enumeration via different responses" – found valid usernames by error messages, used Burp Intruder |
| 2025-11-14 | 19:00 | 19:45 | 0.8 hrs | Authentication (Lab 2) | "Password reset broken logic" – intercepted reset token and changed target username to carlos |
| 2025-11-16 | 13:00 | 13:20 | 0.3 hrs | Access Control (Lab 1) | "Unprotected admin functionality" – found /administrator-panel in page source and deleted carlos |
| 2025-11-17 | 11:00 | 11:30 | 0.5 hrs | Access Control (Lab 2) + reflections | "User role can be modified in user profile" – changed roleid from 1 to 2 in Burp → became admin. Wrote all 6 reflections |
| 2025-11-17 | 12:00 | 12:15 | 0.3 hrs | Final check & submission prep | Updated logbook, checked everything works, ready to submit Grade 1 |
| 2025-11-25 | 14:00 | 14:45 | 0.8 hrs | BookingSystem-Phase1: Docker setup | Downloaded repo, install Docker, run docker-compose up -d, verify app at localhost:8080 |
| 2025-11-26 | 16:00 | 17:30 | 1.5 hrs | BookingSystem-Phase1: Manual testing | Test SQLi (admin'--), XSS (<script>alert(1)</script>), empty fields. |
| 2025-11-27 | 15:00 | 16:30 | 1.5 hrs | BookingSystem-Phase1: ZAP scanning | Install ZAP, run full active scan on /register, attempt to export Markdown report |
| 2025-11-28 | 13:00 | 15:00 | 2.0 hrs | BookingSystem-Phase1: Report + GitHub | Create test_report.md, ZAP_Report.md, pushed to GitHub BookingSystem-Phase1 folder |

**Total hours so far:** **16hours plus**  
**Grade 1 (6 labs) status:** All completed ✅  
**BookingSystem-Phase1 status:**  All completed ✅  

## About
CyberSecurity assignment logbook – tracking time, topics, and outputs.
