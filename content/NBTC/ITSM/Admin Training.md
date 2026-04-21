---
publish: true
---
## โครงสร้างการนำเสนอ: การบริหารจัดการระบบ IT Service Management (Admin Training)

## **ส่วนที่ 1: ภาพรวมสถาปัตยกรรมและการจัดการสภาพแวดล้อม**

- **Microservices Architecture:** ทำความเข้าใจโครงสร้าง 5 Layer ตั้งแต่ Ingress จนถึง External Integration
    
- **หน้าที่ของ Microservices ต่างๆ:** ทำความรู้จัก Service หลัก เช่น Auth, IT Service Management, Jobs (เชื่อมต่อ StarCat11) และ Storage Service
### **ส่วนที่ 2: ขั้นตอนการ Deployment และ CI/CD Pipeline**

- **Pipeline Workflow:** ขั้นตอนการ Build, Test และ Deploy อัตโนมัติผ่าน GitLab CI และ Helm Chart
    
- **การจัดการ Helm Chart:** โครงสร้างโฟลเดอร์ Templates และการตั้งค่าใน `values.yaml`
    
- **ความมั่นคงปลอดภัยของข้อมูลลับ (Secret Management):** การใช้งาน HashiCorp Vault แทนการเก็บ Plain Text ใน Git


### **ส่วนที่ 3: กลยุทธ์การสำรองและกู้คืนข้อมูล (Backup & Restore)**

- **Backup Policy Matrix:** รอบการสำรองข้อมูลและระยะเวลาจัดเก็บ (Retention) ของ K8s, Database และ Object Storage
    
- **การจัดการ Kubernetes Cluster:** การใช้ Velero CLI ในการ Backup และ Disaster Recovery
    
- **การจัดการ Database (PostgreSQL):** ขั้นตอนการทำ On-demand Backup ด้วย `pg_dump` และการ Restore อย่างถูกวิธี
    
- **การจัดการไฟล์เอกสาร:** การสำรองข้อมูล MinIO ด้วยเครื่องมือ `rclone`
    

### **ส่วนที่ 4: การตรวจสอบและเฝ้าระวังระบบ (Observability)**

- **Daily Checklist กับ Grafana:** การตรวจสอบ CPU, Memory, Disk Usage และสถานะสุขภาพของ Pod
    
- **การสืบค้นปัญหาด้วย Kibana (ELK Stack):** เทคนิคการใช้ KQL Query เพื่อดึง Error Log และการเจาะจงราย Service

### **ส่วนที่ 5: มาตรฐานความปลอดภัยและ DevSecOps**

- **Shift-Left Security:** การทำ Image Scanning และ Static Code Analysis ใน Pipeline
    
- **Access Control:** การยืนยันตัวตนผ่าน Active Directory, Google 2FA และการกำหนดสิทธิ์ด้วย RBAC
    
- **Network Security:** การบังคับใช้ HTTPS (TLS/SSL) และการกำหนด Network Policies เพื่อแยก Environment
    

### **ส่วนที่ 6: แนวทางการแก้ไขปัญหา (Troubleshooting)**

- **Incident Response Workflow:** ขั้นตอนมาตรฐานในการวิเคราะห์ปัญหาจาก Monitoring สู่การแยกสาเหตุ (Isolate Issue)
    
- **Case Studies: ปัญหาที่พบบ่อยและวิธีแก้ไข:**
    
    - การรับมือสถานะ `CrashLoopBackOff`
        
    - การแก้ปัญหา 502 Bad Gateway / 504 Gateway Timeout
        
    - การจัดการเมื่อพื้นที่จัดเก็บข้อมูลเต็ม (Disk Pressure)
        
    - การแก้ไขปัญหาการเชื่อมต่อ Database StarCat11 ล้มเหลว


## ประสบการผู้เข้าอบรม
ผู้เข้าอบรมควรเป็น **System Admin หรือ DevOps** ที่มีความเข้าใจเกี่ยวกับสถาปัตยกรรมแบบ **Microservices** และมีประสบการณ์การทำงานบน Linux Command Line มาก่อน มีทักษะด้าน Cloud Native & Containerization,DevOps & CI/CD,Infrastructure & Database,Monitoring & Troubleshooting