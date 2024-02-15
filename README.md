from PIL import Image, ImageDraw

# Resim boyutları
width = 800
height = 600

# Beyaz bir arka plan oluştur
image = Image.new("RGB", (width, height), "white")

# Resmi çizecek nesne oluştur
draw = ImageDraw.Draw(image)

# Ev çatısını çiz
draw.polygon([(50, 300), (400, 50), (750, 300)], fill="brown")

# Ev duvarlarını çiz
draw.rectangle([(50, 300), (750, 600)], fill="lightgray")

# Pencereyi çiz
draw.rectangle([(200, 350), (300, 450)], fill="lightblue")

# Kapıyı çiz
draw.rectangle([(500, 400), (600, 600)], fill="brown")

# Kedi şeklini çiz
draw.ellipse((300, 450, 400, 550), fill="gray")  # Kedinin kafası
draw.ellipse((250, 550, 450, 750), fill="gray")  # Kedinin gövdesi
draw.ellipse((330, 480, 370, 520), fill="white")  # Sol göz
draw.ellipse((370, 480, 410, 520), fill="white")  # Sağ göz
draw.ellipse((340, 500, 360, 520), fill="black")  # Sol gözbebeği
draw.ellipse((380, 500, 400, 520), fill="black")  # Sağ gözbebeği
draw.polygon([(370, 520), (390, 540), (410, 520)], fill="pink")  # Burun
draw.line([(390, 540), (390, 560)], fill="black", width=3)  # Ağız
draw.line([(390, 560), (380, 570)], fill="black", width=3)  # Ağız
draw.line([(390, 560), (400, 570)], fill="black", width=3)  # Ağız
draw.ellipse((320, 470, 340, 490), fill="gray")  # Sol kulak
draw.ellipse((410, 470, 430, 490), fill="gray")  # Sağ kulak
draw.line([(330, 470), (320, 480)], fill="black", width=3)  # Sol kulak çizgisi
draw.line([(350, 470), (340, 480)], fill="black", width=3)  # Sol kulak çizgisi
draw.line([(420, 470), (410, 480)], fill="black", width=3)  # Sağ kulak çizgisi
draw.line([(440, 470), (430, 480)], fill="black", width=3)  # Sağ kulak çizgisi

# Resmi göster
image.show()
