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

Below are 🖼️ screenshots walking through the process of setting up and testing DNS records in a lab environment using Windows Server DNS Manager and PowerShell.



<p align="center"> 
  <img src="https://github.com/user-attachments/assets/1abe92bd-bc15-494f-ad58-cc7701bffebf" width="850"/>
  <figcaption><strong>Figure 1 :</strong> Attempting to ping <code>mainframe</code> before creating its DNS record. The record was not yet present, I need to create a DNS A record for <code>mainframe</code> pointing to DC-1's private IP addres.</figcaption>
    <figcaption><strong>
      
    Figure 1 :
      When Attempting to ping "mainframe" its going to refer to : 
      (1st) Local DNS Cache 
      (2nd) Local Host File 
      (3.) DNS Server  

</figure>

---

<p align="center"> 
  <img src="https://github.com/user-attachments/assets/fd69eb7e-a922-4d5d-afaa-fe2f3e0d46f9" width="850"/>
  <figcaption><strong>Figure 2:</strong> Selecting the "New Host (A or AAAA)" option in DNS Manager to begin defining a hostname-to-IP mapping. This step is required for local DNS resolution.</figcaption>
</p>


---

<p align="center"> 
  <img src="https://github.com/user-attachments/assets/8bcaac26-73d1-4d6a-905a-f6e2c95fe181" width="850"/>
  <figcaption><strong>Figure 3:</strong> Creating a new A record in DNS Manager for <code>mainframe.mydomain.com</code>, pointing to the internal IP <code>10.0.0.4</code>. This record allows internal systems to resolve the hostname to a private IP.</figcaption>
</p>

---

<p align="center"> 
  <img src="https://github.com/user-attachments/assets/8989e023-e8be-4c71-8a89-426c22ba98b0" width="850"/>
  <figcaption><strong>Figure 4:</strong> Running <code>ipconfig /flushdns</code> and <code>/displaydns</code> to clear and verify DNS cache. This is useful to troubleshoot stale DNS entries or refresh recent changes.</figcaption>
  
</p>

---

<p align="center"> 
  <img src="https://github.com/user-attachments/assets/0704ac45-f1e7-4c15-ba82-9fd5a5596d14" width="850"/>
  <figcaption><strong>Figure 5:</strong> Verifying DNS name resolution by pinging <code>mainframe</code>. The system resolves to <code>8.8.8.8</code>, confirming successful alias or A record setup. A notepad note outlines the DNS resolution order.</figcaption>
</p>


---

<p align="center"> 
  <img src="https://github.com/user-attachments/assets/d3c3cc97-2ce7-4c82-a73b-8f1b675f4a66" width="850"/>
  <figcaption><strong>Figure 6:</strong> Right-clicking in DNS Manager to create a new CNAME (alias) record. This step maps a hostname to another domain, aiding flexible name resolution.</figcaption>
</p>




---

## 💡 Key Takeaways
✅ Understanding of core DNS record types and their purposes  
✅ Learned how to troubleshoot name resolution issues using command-line tools  
✅ Realized how local DNS caching can affect immediate changes in the environment  
✅ Reinforced how client-server DNS interactions work in domain-based networks

---



