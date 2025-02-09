import datetime as dt

print("\n",5*"="+"Welcome to Calculator to Count Your Age"+5*"=")

print(f"Silahkan masukkan tanggal, bulan dan tahun")
nama = str(input("Nama \t\t: ") )
tanggal = int(input("Tanggal \t: "))
bulan = int(input("Bulan \t\t: "))
tahun = int(input("Tahun \t\t: "))
tanggal_lahir = dt.date(tahun,bulan,tanggal)
print(f"tanggal lahir {nama} adalah: {tanggal_lahir}")

hari_ini = dt.date.today()
print(f"hari ini tanggal: {hari_ini}")
umur_hari = hari_ini - tanggal_lahir
umur_tahun = umur_hari.days // 365 
umur_bulan_sisa = (umur_hari.days % 365) // 30
print(f"harinya adalah : {tanggal_lahir:%A}")
print(f"Umur {nama} adalah: {umur_tahun} tahun, {umur_bulan_sisa} bulan")
