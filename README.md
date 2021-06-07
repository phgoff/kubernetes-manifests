## Commands
*ใส่ **-n [name of namespace]** เพื่อดู resources ที่อยู่ใน namespace นั้น ๆ
```
  kubectl get services                          # แสดง service ทั้งหมดใน default namespace
  kubectl get deployment                        # แสดง deployment ทั้งหมด
  kubectl get deployment my-dep                 # แสดง my-dep deployment
  kubectl get pods --all-namespaces             # แสดง pods ทั้งหมดที่อยู่ในทุก ๆ namespace
  kubectl get pods -o wide                      # แสดง pods ทั้งหมดพร้อมรายละเอียดต่าง ๆ
  kubectl get pods                              # แสดง pods ทั้งหมด
  kubectl get pod my-pod -o yaml                # แสดง my-pod ในรูปแบบ yaml
```

#### การติดต่อกับ pod 
```
  kubectl exec -it my-pod -- sh                 # เข้าไปยัง terminal ของ my-pod ด้วย sh
  kubectl exec my-pod -- ls ./example           # แสดงไฟล์ที่อยู่ในพาท example
```

#### การดูข้อมูล log ของ pod
```
  kubectl logs my-pod                           # แสดงข้อมูล log ที่่ผ่านมาของ my-pod
  kubectl logs -f my-pod                        # แสดงข้อมูล log แบบการแสดงผลอย่างต่อเนื่อง
```
