# Desafios e Limitações do VCCX (CONS)

Embora o VCCX ofereça qualidade superior para o Português Brasileiro, ele traz alguns trade-offs em comparação a métodos mais simples.

### 1. Curva de Aprendizado na Gravação
Diferente de métodos "diretos" como CV ou VCV simples, o VCCX exige um ritmo específico de gravação.
- **O Desafio:** O formato `ba_ba_b` (CVVC) ou `bl_bl` (Cluster) requer controle de respiração e tempo para garantir que a consoante final ou o encontro consonantal fiquem limpos.
- **Impacto:** Iniciantes podem precisar de algumas tentativas até pegar a fluidez correta da gravação.

### 2. Dependência de Phonemizer/Plugin (OpenUtau)
O VCCX foi desenhado para brilhar no OpenUtau.
- **O Desafio:** Para extrair o máximo do banco (fallback automático, timing inteligente, conversão X-SAMPA), é **obrigatório** o uso do `PortugueseBrazilVCCXPhonemizer.dll`.
- **Impacto:** Usuários do UTAU Legacy (vanilla) terão muito mais trabalho manual para configurar os usts ou dependerão de plugins externos menos integrados.

### 3. Maior Número de Amostras
Para garantir a cobertura fonética completa, o VCCX é mais extenso que um banco básico.
- **O Desafio:** São cerca de **652 amostras** para um banco completo (com todos os clusters e VCVs).
- **Impacto:** O tempo de gravação é maior do que bancos simples (embora menor que VCVs completos de outras línguas). Vozes cansadas podem sofrer para gravar tudo em uma sessão.

### 4. Complexidade de oto.ini (Se feito à mão)
Configurar um VCCX do zero sem ferramentas pode ser assustador.
- **O Desafio:** Cada tipo de amostra (CVVC, VCV, Cluster) tem regras de *overlap* e *preutterance* ligeiramente diferentes.
- **Impacto:** É altamente recomendado usar grandes utilitários (como o do Copaiba Lexicon/SetParam) ou ter conhecimento sólido de oto.ini para não "quebrar" as transições.

### Resumo
O VCCX não é "plug-and-play" no sentido de "gravar qualquer coisa de qualquer jeito". Ele exige **compromisso com a qualidade e ordem**. Se você quer apenas um banco rápido de 50 amostras para brincar, o VCCX pode parecer um esforço exagerado e sem necessidade. Mas se busca fluídez, o esforço paga a conta.
