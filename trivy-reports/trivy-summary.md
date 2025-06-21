# 🔐 Trivy Scan Summary

## 📦 Container Image (mahipalsinghjhala/devproject:latest – Ubuntu 20.04)
- **Total Vulnerabilities:** 8
- **Severity Breakdown:**
  - LOW: 0
  - MEDIUM: 8
  - HIGH: 0
  - CRITICAL: 0

### Example:
| Library     | Vulnerability | Severity | Installed | Fixed | Description |
|-------------|---------------|----------|-----------|-------|-------------|
| libc-bin    | CVE-2025-4802 | MEDIUM   | 2.31-0ubuntu9.17 | 2.31-0ubuntu9.18 | glibc dlopen misuses LD_LIBRARY_PATH |
| libsqlite3-0 | CVE-2025-29088 | MEDIUM  | 3.31.1-4ubuntu0.6 | 3.31.1-4ubuntu0.7 | SQLite DoS vulnerability |

---

## ⚙️ Application Dependencies (pom.xml)
- **Total Vulnerabilities:** 69
- **Severity Breakdown:**
  - LOW: 3
  - MEDIUM: 25
  - HIGH: 30
  - CRITICAL: 11

### Example:
| Library                                | Vulnerability | Severity | Fixed Version | Description |
|----------------------------------------|---------------|----------|----------------|-------------|
| ch.qos.logback:logback-classic         | CVE-2023-6378 | HIGH     | 1.2.13         | Logback deserialization vulnerability |
| com.h2database:h2                      | CVE-2021-42392| CRITICAL | 2.0.206        | Remote Code Execution via H2 console |
| org.springframework:spring-web         | CVE-2016-1000027 | CRITICAL | 6.0.0         | Java deserialization vulnerability |

---

## 🧠 Recommendation

- Upgrade libraries to patched versions listed in the report.
- Address critical vulnerabilities immediately, especially those involving RCE and DoS.
- Refer to the full HTML reports for the complete list of CVEs.

---

🔗 For full details, refer to:
- `trivy-report-container.html`
- `trivy-report-pom.html`