import requests
from bs4 import BeautifulSoup

# Giriş məlumatları (əgər tələb olunursa)
login_url = "https://sap.aztu.edu.az/login.php"
attendance_url = "https://sap.aztu.edu.az/studies/lecture_attend.php?lec_open_idx=60461&lecture_code=4138&sem_code=20242"

# Giriş üçün istifadəçi məlumatlarını daxil edin
login_data = {
    "username": "istifadeci_adi",  # Buraya istifadəçi adınızı yazın
    "password": "sifre",          # Buraya şifrənizi yazın
}

# Sessiyanı saxlayan obyekt yaradılır
session = requests.Session()

# Giriş sorğusu göndərilir
login_response = session.post(login_url, data=login_data)

# Girişin uğurlu olub-olmadığını yoxlayın
if login_response.status_code == 200 and "dashboard" in login_response.text:
    print("Giriş uğurludur.")
else:
    print("Giriş uğursuz oldu.")
    exit()

# Davamiyyət səhifəsini əldə etmək
response = session.get(attendance_url)

# Səhifənin uğurla alınıb-alınmadığını yoxlayın
if response.status_code == 200:
    soup = BeautifulSoup(response.text, "html.parser")
    # Davamiyyət məlumatlarını çıxarmaq üçün uyğun HTML elementlərini tapın
    attendance_data = soup.find_all("table")  # Davamiyyət məlumatlarının olduğu cədvəl
    for table in attendance_data:
        print(table.text)
else:
    print("Davamiyyət səhifəsi əldə edilə bilmədi.")
