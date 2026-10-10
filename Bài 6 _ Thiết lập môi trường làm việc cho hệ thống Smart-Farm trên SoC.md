**các câu lệnh**  
mkdir \~\\smart-farm\\bin, \~\\smart-farm\\config, \~\\smart-farm\\data  
New-Item \-ItemType File \-Path \~\\smart-farm\\config\\.env  
attrib \+h \~\\smart-farm\\config\\.env  
Copy-Item \-Path .\\Public\\template.ps1 \-Destination \~\\smart-farm\\bin\\pump\_control.ps1  
Get-ChildItem \-Path \~\\smart-farm \-Recurse \-Force

**Khi gặp lỗi:**  
Start-Process powershell \-Verb RunAs

**IPO:**  
**Input:** Thư mục gốc \~, mật khẩu, file template.ps1.  
**Process:** Dùng mkdir tạo thư mục, New-Item và attrib \+h tạo file ẩn, Copy-Item sao chép/đổi tên, Get-ChildItem kiểm tra.  
**Output:** Hệ thống thư mục smart-farm hoàn chỉnh và file mật khẩu đã ẩn.