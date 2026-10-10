# -
โปรแกรมสำหรับคำนวนราคาและจำนวนของสินค้า โดยการใช้ภาษา Python ในการเขียนโค้ด และ ใช้ AI ในการช่วยเหลือ
total = 0

while True:
    print("\n===== โปรแกรมคำนวณราคาสินค้า =====")

    price = float(input("กรอกราคาสินค้า: "))
    quantity = int(input("กรอกจำนวนสินค้า: "))

    # คำนวณราคาสินค้า
    subtotal = price * quantity

    # ตรวจสอบส่วนลด
    if subtotal >= 1000:
        discount = subtotal * 0.10
    elif subtotal >= 500:
        discount = subtotal * 0.05
    else:
        discount = 0

    final_price = subtotal - discount
    total += final_price

    print("\n--- ผลลัพธ์ ---")
    print("ราคาสินค้า:", price, "บาท")
    print("จำนวน:", quantity, "ชิ้น")
    print("ราคาก่อนลด:", subtotal, "บาท")
    print("ส่วนลด:", discount, "บาท")
    print("ราคาที่ต้องจ่าย:", final_price, "บาท")

    # ถามว่าต้องการเพิ่มสินค้าอีกหรือไม่
    again = input("\nต้องการเพิ่มสินค้าอีกหรือไม่ (y/n): ")

    if again.lower() == "n":
        break

print("\n==============================")
print("ยอดรวมทั้งหมด:", total, "บาท")
print("==============================")
print("ขอบคุณที่ใช้บริการ")
