İzah
Giriş Prosesi:
Sistemə giriş tələb olunursa, login_url vasitəsilə istifadəçi adı və şifrə göndərilir. Sessiya saxlanılır ki, növbəti sorğularda istifadə olunsun.

Davamiyyət Məlumatlarının Çıxarılması:
BeautifulSoup kitabxanası HTML səhifəni analiz etmək üçün istifadə olunur. Cədvəl (<table>) və ya digər HTML elementlər vasitəsilə davamiyyət məlumatları çıxarılır.

Tələblər:

requests və beautifulsoup4 kitabxanalarını quraşdırmaq:
bash
Copy code
pip install requests beautifulsoup4
Vacib Qeyd
Əgər sistem CAPTCHA tələb edirsə, bu kod işləməyə bilər. Belə halda CAPTCHA-nı avtomatlaşdırmaq üçün əlavə kitabxanalardan istifadə etmək lazımdır.
Şəxsi məlumatlarınızı (istifadəçi adı və şifrə) qoruyun. Kodda birbaşa daxil etmək əvəzinə, konfiqurasiya fayllarından və ya mühit dəyişənlərindən istifadə edin.
