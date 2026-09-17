# Wii Will Rock You — 1.0.0

**Fernando "FLX" Colares**

Versão estável do bridge de guitarra Wii para Windows.

Grande demais pro Github pelo visto
https://drive.google.com/file/d/1pjbkPTspSNKcKJMD5KpeVmxLs938I3x4/view?usp=drive_link

aproveitem

## Modos de saída

### Modo Guitarra

Cria uma guitarra virtual XInput com subtype **GUITAR (0x06)** usando VIIPER/USBip. O HUD confirma se o Windows reconheceu o subtype correto.

Mapeamento padrão:

- Frets: A / B / Y / X / LB
- Strum: D-Pad cima / baixo
- Whammy: Right Stick X
- Tilt / Star Power: Right Stick Y
- Analógico físico: Left Stick
- + / -: Start / Back

Compatibilidade-alvo do Modo Guitarra: **Clone Hero, Guitar Hero e Frets on Fire / FoFiX**, além de jogos que aceitem guitarra XInput equivalente.

### Modo Controle

Cria um gamepad Xbox 360 virtual pelo ViGEm. O mapeamento é configurável para uso mais universal. Se o Whammy estiver associado a um botão digital, ele só é acionado ao atingir o limiar configurado, **60% por padrão**.

## Primeira ativação do Modo Guitarra

O programa pode precisar preparar o VIIPER portátil e o `usbip-win2`. Como o USBip instala um driver de kernel, a instalação só é iniciada após confirmação explícita. Uma reinicialização do Windows pode ser necessária na primeira configuração.

Se o USBip já estiver instalado, o Wii Will Rock You apenas verifica a instalação existente e não abre o instalador novamente.

## Instalação / execução

Extraia o ZIP e execute:

`INICIAR.bat`

Na primeira execução, o script verifica o .NET 8 SDK, baixa uma cópia local se necessário, restaura as dependências e publica uma versão Windows x64 autocontida.

O executável final fica em:

`publish\WiiWillRockYou.exe`

Na mesma pasta, o build também copia `LEIA-ME - INSTRUCOES.txt` com o passo a passo básico de conexão, modos de saída e os componentes que o programa prepara automaticamente.

## Uso básico

1. Conecte o Wiimote no Windows.
2. Abra o Wii Will Rock You.
3. Aguarde a inicialização automática da guitarra.
4. Escolha **MODO GUITARRA** ou **MODO CONTROLE**.
5. Ative a saída de jogo.
6. No Modo Guitarra, confirme no HUD `GUITAR (0x06) CONFIRMADO`.

O painel **DETALHES** mantém diagnóstico, telemetria, calibração e log fora do HUD principal para deixar a interface mais limpa durante o uso.
