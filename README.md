# MongoDB_replication_and_sharding_by_docker (thay vì như tutorial thì em làm theo thao tác với docker)

## Replication:

### Cài image MongoDB:
<img width="1149" height="609" alt="image" src="https://github.com/user-attachments/assets/1bc42fb2-e474-4a9a-b854-4f4d76c2c309" />

### Khởi động container MongoDB với port mặc định và kết nối vào container:
<img width="1136" height="521" alt="image" src="https://github.com/user-attachments/assets/0cf485cf-104f-4f15-b613-22d14609e146" />


### Tạo Network Docer dành cho các node mongoDB và khởi tạo 3 container làm Replica Set 
<img width="1086" height="227" alt="image" src="https://github.com/user-attachments/assets/a82b0cf2-e889-47ac-803a-539e4572d353" />
<img width="2109" height="953" alt="image" src="https://github.com/user-attachments/assets/59a88998-d0da-4f42-9894-4896e9cc3af0" />


### Khởi tạo cấu hình Replica Set:
<img width="1132" height="508" alt="image" src="https://github.com/user-attachments/assets/5e32b9f5-68b4-4c79-8775-5121089431cf" />

##### Khai báo các node thành viên:
<img width="1139" height="555" alt="image" src="https://github.com/user-attachments/assets/5b0555eb-539b-4c8b-9cc8-d35a1e0d14bc" />

##### Thêm dữ liệu và thử xem dữ liệu có replicate sang secondary không:
<img width="845" height="233" alt="image" src="https://github.com/user-attachments/assets/75682144-212b-49ce-930d-9ab905942e00" />

##### kiểm tra với node2:
<img width="1129" height="505" alt="image" src="https://github.com/user-attachments/assets/5ee6f0e3-7de4-4ba1-adde-662ee47897c3" />
<img width="1190" height="460" alt="image" src="https://github.com/user-attachments/assets/c09ffe18-3f21-49bf-8fd2-0e036eac83bf" />

##### Thử dùng mongo1 (primary) xong kiểm tra lúc này một trong các secondary sẽ tự động chuyển thành primary:
<img width="1152" height="508" alt="image" src="https://github.com/user-attachments/assets/3842e4de-8aa1-4657-a7c2-2436b813d3bb" />

###### Lúc này mongo2 từ secondary đã thành primary:
<img width="876" height="478" alt="image" src="https://github.com/user-attachments/assets/4ffded50-b8bc-46ea-8531-6cae4f0b7e72" />

## Sharding:

### Tạo network docer cho cluster
<img width="656" height="62" alt="image" src="https://github.com/user-attachments/assets/a72dfc82-35a3-4b5e-abae-b71988645900" />

### khởi động config server và các shard server
<img width="1145" height="230" alt="image" src="https://github.com/user-attachments/assets/245ce4a6-a23c-4a88-9dde-56efbb8d2144" />
<img width="2134" height="260" alt="image" src="https://github.com/user-attachments/assets/5d30a4ee-9b5f-40ce-80e3-8f1eccb41f44" />


### khởi động mongos:
<img width="1128" height="140" alt="image" src="https://github.com/user-attachments/assets/264bb597-57fd-4e3b-a2ce-d53fe6a14539" />

### khởi tạo config server replica set
<img width="1139" height="464" alt="image" src="https://github.com/user-attachments/assets/7fc07fa6-83fa-4cc2-b147-839752d80c3a" />


### tạo replica set cho từng shard:
<img width="1124" height="424" alt="image" src="https://github.com/user-attachments/assets/6b0bfec2-a6e1-4239-b564-60fd6b9da026" />
<img width="1132" height="476" alt="image" src="https://github.com/user-attachments/assets/d59325cf-a1fc-4834-b144-82f09388a52e" />

### kết nối lại mongos và cấu hình sharding
<img width="1155" height="274" alt="image" src="https://github.com/user-attachments/assets/fd950f24-a9f1-4410-946a-67af6cfbb0ff" />
<img width="740" height="510" alt="image" src="https://github.com/user-attachments/assets/5d416c7e-99b9-4b63-89b6-e4badc711afe" />
<img width="763" height="525" alt="image" src="https://github.com/user-attachments/assets/d50b3e0d-dddd-45e4-ba89-cfdca88914bb" />
<img width="767" height="293" alt="image" src="https://github.com/user-attachments/assets/65ad9749-c2c3-4c87-8a94-0494e447be4f" />



