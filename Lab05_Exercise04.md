# Lab 5 Exercise 4

## Fields declaration and initialization


1. สร้าง console application project

```
dotnet new console --name Lab05_Ex04
```
2. เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
var myObj = new MyClass();

System.Console.WriteLine($"Default integer      F1 = {myObj.F1}");  //Implicit fields initialization
System.Console.WriteLine($"Default string       F2 = {myObj.F2}");
System.Console.WriteLine($"Initialized integer  F3 = {myObj.F3}");  //Explicit field initialization
System.Console.WriteLine($"Initialized string   F4 = {myObj.F4}");

class MyClass
{
    public int F1;
    public string F2;
    public int F3 = 100;
    public string F4 = "ASDF";
}
```

3. Build project โดยการใช้คำสั่ง

```
dotnet build  Lab05_Ex04
```

4. บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-05/assets/144195555/059f07bb-c44b-40a4-895f-5bfada86b7fd)
### โปรแกรมสามารถ Build ได้ แต่โปรแกรมจะแจ้ง ไม่ได่ระบุค่า int F1 กับ string F2 จะให้เป็น ค่า 0 หรือ null แทนเป็น ค่าเริ่มต้น
5. Run project โดยการใช้คำสั่ง

```
dotnet run --project Lab05_Ex04
```

6. บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-05/assets/144195555/d9cd0911-366b-4e5d-9d3c-f931a4feb45f)
### โปรแกรมสามารถ Run ได้ปกติโดยจะแสดงผลตาม Type ค่าที่กำหนด ถ้าไม่ได้กำหนดจะเป็น 0 หรือ null

7. อธิบายสิ่งที่พบในการทดลอง
### โปรแกรมจะแสดงผล F1 = 0 F2 = null ตามชนิด Type เป็น Implicit fields initialization เพราะไม่ได้กำหนดค่า
### โปรแกรมจะแสดงผล F3 = 100 F4 = ASDF ตามชนิด Type เป็น Explicit field initialization เพราะกำหนดค่า

