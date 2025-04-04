<p align="center">
<img src="https://github.com/user-attachments/assets/b7ad7586-1b3b-4a5b-8fd9-40774e4d447d" 
</p>


# 🌐 DNS Configuration & Troubleshooting

> In this lab, I explored how DNS functions within a domain environment by working directly with a Windows Server domain controller and client machine. I gained hands-on experience in creating and managing DNS records, diagnosing resolution issues, and understanding how local caching affects network behavior.

---

## 🧰 Skills & Tools Used
- Windows Server 2022  
- DNS Manager  
- Windows 10 Client  
- `ping`, `ipconfig`, `nslookup`  

---

## 🧩 Lab Focus Areas

### 🔸 DNS A-Records
Created a custom A-record pointing a hostname to an internal IP address. Verified that name resolution worked properly from the client machine after configuration.

### 🔸 CNAME Records
Set up a CNAME record to alias a hostname to an external domain (e.g., Google). Tested successful resolution using `ping` and `nslookup`.

### 🔸 DNS Caching Behavior
Observed how DNS cache stores outdated records temporarily, leading to incorrect resolution. Learned how to inspect and clear the cache using command-line tools to refresh DNS lookups.

---

## 🖼️ Screenshots  
*(Insert screenshots showing A-record and CNAME configuration, successful resolution, and cache output)*

---

## 💡 Key Takeaways
✅ Understanding of core DNS record types and their purposes  
✅ Learned how to troubleshoot name resolution issues using command-line tools  
✅ Realized how local DNS caching can affect immediate changes in the environment  
✅ Reinforced how client-server DNS interactions work in domain-based networks

---



