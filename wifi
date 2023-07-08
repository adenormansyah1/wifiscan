import subprocess
from pyfiglet import Figlet

# Menggunakan modul pyfiglet untuk membuat teks dalam ASCII art
custom_font = Figlet(font='slant')
ascii_art = custom_font.renderText('Script Wifi Scan Powered By Ade Normansyah')

print(ascii_art)

def scan_wifi():
    command = "termux-wifi-scaninfo"
    result = subprocess.check_output(command, shell=True)
    return result.decode("utf-8")

def connect_to_wifi(ssid, password):
    command = f"termux-wifi-connect -s {ssid} -p {password}"
    result = subprocess.check_output(command, shell=True)
    return result.decode("utf-8")

def disconnect_wifi():
    command = "termux-wifi-disconnect"
    result = subprocess.check_output(command, shell=True)
    return result.decode("utf-8")

def view_saved_wifi_passwords():
    command = "termux-wifi-connectioninfo"
    result = subprocess.check_output(command, shell=True)
    return result.decode("utf-8")

# Mencari jaringan WiFi yang tersedia
wifi_networks = scan_wifi()
print("Daftar jaringan WiFi yang tersedia:")
print(wifi_networks)

# Menghubungkan ke jaringan WiFi tertentu
ssid = input("Masukkan nama jaringan WiFi (SSID): ")
password = input("Masukkan password WiFi: ")
result = connect_to_wifi(ssid, password)
print(result)

# Memutuskan koneksi WiFi
result = disconnect_wifi()
print(result)

# Melihat kata sandi WiFi yang tersimpan
wifi_passwords = view_saved_wifi_passwords()
print("Kata sandi WiFi yang tersimpan:")
print(wifi_passwords)
