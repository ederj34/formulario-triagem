#from bs4 import BeautifulSoup

# Reabrir o HTML funcional existente
with open("/mnt/data/formulario_funcional_whatsapp.html", "r", encoding="utf-8") as f:
    html = f.read()

soup = BeautifulSoup(html, "html.parser")

# Remover todos os botões anteriores, deixando apenas um
buttons = soup.find_all("button")
for i, btn in enumerate(buttons):
    if i == 0:
        continue  # manter apenas o primeiro
    btn.decompose()

# Salvar novamente com apenas um botão de envio
formulario_unico_botao = "/mnt/data/formulario_apenas_um_botao.html"
with open(formulario_unico_botao, "w", encoding="utf-8") as f:
    f.write(str(soup))

formulario_unico_botao
