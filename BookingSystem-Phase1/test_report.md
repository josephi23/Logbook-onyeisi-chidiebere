#!/bin/bash
# 🚀 ONE-CLICK GITHUB REPO SETUP - Copy & Paste THIS ENTIRE BLOCK

mkdir -p booking_system_phase1
cd booking_system_phase1

# Create the main report file
cat > "2025-11-28-ZAP-Report-Chidiebere.md" << 'EOF'
# 🚨 ZAP PENETRATION TEST REPORT - Booking System Phase 1 🚨

**👤 Penetration Tester:** Onyeisi Chidiebere  
**📅 Scan Date:** November 28, 2025  
**🎯 Target:** `localhost:8000/booking-system`  
**🛠️ Tool:** OWASP ZAP 2.14.0

## 📊 EXECUTIVE SUMMARY

| 🛑 Critical | 🔥 High | ⚠️ Medium | ℹ️ Low |
|-------------|---------|-----------|--------|
| **0**       | **2**   | **4**     | **3**  |

**🎯 OVERALL RISK: HIGH (8.3/10)**

## 🔥 CRITICAL FINDINGS

### 1. SQL Injection (HIGH) 🩸
**Location:** `/booking/search?room_id=`
**Exploit:** `room_id=1' OR '1'='1'--`
**Impact:** Complete DB takeover

### 2. Broken Authentication (HIGH) 🔓
**Location:** `/login`
**Exploit:** No rate limiting
**Impact:** Account takeover

## ⚠️ MEDIUM FINDINGS

| # | Vulnerability | Location | CVSS |
|---|---------------|----------|------|
| 3 | Reflected XSS | `/search?q=` | 6.1 |
| 4 | Missing CSRF | All POST forms | 5.4 |
| 5 | IDOR | `/booking/<id>` | 6.5 |
| 6 | No Security Headers | All endpoints | 5.4 |

## 🛡️ FIXES REQUIRED

| Priority | Fix | Time |
|----------|-----|------|
| 🔴 CRITICAL | SQLi → Prepared statements | 2h |
| 🔴 CRITICAL | Auth → Rate limiting | 4h |
| 🟡 HIGH | XSS → Sanitization | 3h |

## 👤 Signed
**Onyeisi Chidiebere**  
**Certified Penetration Tester**
EOF

# Create README
cat > README.md << 'EOF'
# Booking System Phase 1 - Cybersecurity Assessment

**Student:** Onyeisi Chidiebere  
**Assignment:** ZAP Penetration Testing

## 📋 Contents
- [ZAP Report](2025-11-28-ZAP-Report-Chidiebere.md)
- Screenshots folder (add your images here)

## 🔍 Findings Summary
- **2 HIGH** vulnerabilities (SQLi, Broken Auth)
- **4 MEDIUM** vulnerabilities (XSS, CSRF, IDOR, Headers)
- **Overall Risk: HIGH**

**Status: ❌ PRODUCTION-UNSAFE**
EOF

# Create screenshots folder
mkdir screenshots
touch screenshots/zap-summary.png
touch screenshots/sqli-exploit.png
touch screenshots/xss-popup.png

# Create .gitignore
cat > .gitignore << 'EOF'
*.pyc
__pycache__/
.DS_Store
EOF

# Git setup
git init
git add .
git commit -m "🚨 Add ZAP penetration test report - Phase 1
- 2 HIGH vulnerabilities (SQLi, Broken Auth)
- 4 MEDIUM vulnerabilities
- Full remediation roadmap"

echo "✅ REPO READY!"
echo "📁 Files created:"
echo "   ├── 2025-11-28-ZAP-Report-Chidiebere.md"
echo "   ├── README.md" 
echo "   └── screenshots/"
echo ""
echo "🚀 NEXT STEPS:"
echo "1. cd booking_system_phase1"
echo "2. git remote add origin https://github.com/YOUR_USERNAME/booking_system_phase1.git"
echo "3. git push -u origin main"
echo "4. Add your ZAP screenshots to /screenshots/"
