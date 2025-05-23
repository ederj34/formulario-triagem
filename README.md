# Formulário Jurídico – Rafael Nunes Advogados

Formulário automatizado com envio para WhatsApp, planilha e geração de PDF.
from bs4 import BeautifulSoup

# Reabrir a versão mais robusta
with open("/mnt/data/formulario_final_corrigido_robusto.html", "r", encoding="utf-8") as f:
    html = f.read()

soup = BeautifulSoup(html, "html.parser")

# Adicionar texto de rodapé explicativo e criar link fictício de domínio
footer = BeautifulSoup("""
<footer style="text-align: center; padding: 20px; font-size: 14px; color: #ccc;">
  <p>Este formulário está disponível em <strong>form.rafaelnunes.adv.br</strong></p>
  <p>© 2024 Rafael Nunes Advogados. Todos os direitos reservados.</p>
</footer>
""", "html.parser")

# Inserir rodapé no final do <body>
soup.body.append(footer)

# Salvar versão final com rodapé institucional e domínio fictício
final_com_footer = "/mnt/data/formulario_publicavel_com_dominio.html"
with open(final_com_footer, "w", encoding="utf-8") as f:
    f.write(str(soup))

final_com_footer
