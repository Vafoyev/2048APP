# 2048 O'yini (C# Windows Forms)

Ushbu loyiha mashhur "2048" o'yinining C# dasturlash tilida Windows Forms texnologiyasidan foydalanib yaratilgan versiyasidir.

## Loyiha Haqida

Bu o'yin foydalanuvchiga raqamli plitkalarni surish orqali bir xil qiymatdagi plitkalarni birlashtirish va imkon qadar yuqori natijaga (2048 yoki undan katta plitka) erishish imkoniyatini beradi. Loyiha o'quv maqsadlarida, C# va Windows Forms bilan ishlash ko'nikmalarini mustahkamlash uchun yaratilgan.

## Muallif

*   **Dasturchi:** Vafoyev Isobek 
*   **Asl "2048" o'yini muallifi (agar clone qilingan bo'lsa):** Lukasz Jakowski (Ushbu loyiha uning g'oyasiga asoslangan)
*   **Ishlab chiqilgan sana :** 2025 yil

## Funksionallik

*   **O'yin Maydoni:** Standart 4x4 o'lchamdagi o'yin maydoni.
*   **Boshqaruv:** Klaviatura yordamida (W, A, S, D yoki strelkali tugmalar) plitkalarni surish.
*   **Plitkalarni Birlashtirish:** Bir xil qiymatdagi ikkita plitka to'qnashganda, ular bitta, qiymati ikkilangan plitkaga birlashadi.
*   **Yangi Plitkalar:** Har bir muvaffaqiyatli harakatdan so'ng o'yin maydonidagi tasodifiy bo'sh katakka yangi plitka (qiymati 2 yoki 4) paydo bo'ladi.
*   **Ochkolar (Score):** Har bir plitka birlashganda ochkolar hisoblanadi.
*   **Eng Yaxshi Natija (Best):** O'yin davomida erishilgan eng yuqori ochko saqlanib qoladi (dastur yopilguncha).
*   **Yangi O'yin (New Game):** Joriy o'yinni to'xtatib, yangisini boshlash imkoniyati.
*   **Haqida (About):** Dastur va muallif haqida qisqacha ma'lumot.
*   **O'yin Tugashi (Game Over):** O'yin maydonida bo'sh katak qolmaganda va hech qanday plitkani birlashtirish imkoni bo'lmaganda o'yin tugaydi.

## Ishlatilgan Texnologiyalar

*   **Dasturlash Tili:** C#
*   **Platforma:** .NET Framework (masalan, .NET Framework 4.8)
*   **Foydalanuvchi Interfeysi:** Windows Forms
*   **Grafika:** System.Drawing (GDI+) kutubxonasi orqali dinamik chizish
*   **Ishlab Chiqish Muhiti:** Microsoft Visual Studio

## Loyiha Tuzilmasi (Asosiy Fayllar)

*   `Main.cs`: Asosiy oyna logikasi, hodisalarni qayta ishlash.
*   `Main.Designer.cs`: Form dizayneri tomonidan generatsiya qilingan kod, vizual elementlarning sozlamalari.
*   `Game.cs`: Asosiy o'yin logikasi, o'yin maydoni, plitkalar harakati, ochkolarni hisoblash, chizish amallari.
*   `Button.cs`: (Agar mavjud bo'lsa) O'yindagi interaktiv tugmalar uchun maxsus klass.
*   `CFG.cs`: (Agar mavjud bo'lsa) Ba'zi konfiguratsiya sozlamalari uchun klass.
*   `Program.cs`: Dasturning kirish nuqtasi (`Main()` funksiyasi).
*   `images/` papkasi: O'yin uchun ishlatiladigan `.png` formatidagi rasm fayllari.

## O'rnatish va Ishga Tushirish

1.  Loyihani clone qiling yoki yuklab oling.
2.  Microsoft Visual Studio'da `.sln` faylini oching.
3.  Agar kerak bo'lsa, .NET Frameworkning mos versiyasi o'rnatilganligiga ishonch hosil qiling.
4.  Loyihani "Build" qiling (`Build -> Build Solution`).
5.  Dasturni ishga tushiring (`Debug -> Start Debugging` yoki `Ctrl+F5`).

**Boshqalarga yuborish uchun:**
Loyihani "Release" konfiguratsiyasida "Build" qiling. `bin/Release` papkasidagi `.exe` faylini va uning yoniga `images` papkasini (barcha rasmlari bilan) joylashtirib, birgalikda yuboring.

## Algoritmning Asosiy Jihatlari

1.  **Boshlash:** 4x4 o'lchamli bo'sh o'yin maydoni yaratiladi va tasodifiy 2 ta plitka joylashtiriladi.
2.  **Harakat:** Foydalanuvchi klaviatura orqali yo'nalishni tanlaydi.
3.  **Surish va Birlashtirish:** Tanlangan yo'nalishda barcha plitkalar maksimal darajada suriladi. Agar surilish paytida bir xil qiymatli ikkita plitka uchrashsa, ular bitta, qiymati ikkilangan plitkaga aylanadi va ochko qo'shiladi. Birlashgan plitka shu harakatda boshqa plitka bilan qayta birlashmaydi.
4.  **Yangi Plitka:** Muvaffaqiyatli harakatdan so'ng (biror plitka surilgan yoki birlashgan bo'lsa), o'yin maydonidagi tasodifiy bo'sh katakka yangi plitka (odatda 2, ba'zan 4) qo'shiladi.
5.  **O'yin Tugashi:** Agar o'yin maydonida bo'sh katak qolmasa va hech qanday qo'shni plitkalarni birlashtirish imkoni bo'lmasa, o'yin tugaydi.
6.  **Chizish:** Har bir o'zgarishdan so'ng o'yin maydoni, ochkolar va boshqa elementlar ekranga qayta chiziladi. Miltillashni kamaytirish uchun double buffering usuli qo'llanilgan (xotiradagi `Bitmap`ga chizib, keyin uni ekranga chiqarish).

## Kelajakdagi Mumkin Bo'lgan Yaxshilanishlar

*   Ovoz effektlarini qo'shish.
*   Turli o'lchamdagi o'yin maydonlarini tanlash imkoniyati.
*   O'yinni saqlash va davom ettirish funksiyasi.
*   Animatsiyalar bilan silliqroq plitka harakatlari.
*   Turli mavzular (ranglar va shriftlar).

---

Umid qilamanki, bu `README.md` namunasi sizga yoqadi va foydali bo'ladi!
