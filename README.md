# Controle ESP32-C3 em 3D

Visualizador 3D interativo de um controle sem fio com ESP32-C3 SuperMini: câmera livre, vista explodida e ficha técnica de cada componente.

## Componentes

| Componente | Função |
|---|---|
| ESP32-C3 SuperMini | Microcontrolador (RISC-V 160 MHz, Wi-Fi e Bluetooth 5 LE) |
| Placa de expansão | Fileiras G · V · S para cada GPIO, regulador AMS1117-3.3, entrada JST |
| Analógico | Joystick de 2 eixos (VRx, VRy) com botão (SW) |
| Bateria Li-Po 850 mAh | 3,7 V com circuito de proteção |
| Carcaça | Duas metades (frontal e traseira) |

## Como usar

- **Arrastar:** gira a câmera · **botão direito:** move · **rolar:** zoom
- **Explodir vista / Fechar vista** ou a barra **Abertura** para abrir parcialmente
- **Clique numa peça** (ou na lista) para ver as especificações; **Isolar peça** destaca só ela
- Atalhos: `E` abre/fecha, `R` recentraliza, `Esc` fecha a ficha

## Rodar localmente

O modelo é carregado via `fetch`, então a página precisa de um servidor (não abre direto do arquivo):

```bash
python3 -m http.server 8765
```

Depois abra <http://localhost:8765>.

## Arquivos

- `index.html` — a página (three.js r169 via CDN, sem build)
- `controle.glb` — o modelo 3D: 14 peças móveis com os dados da vista explodida em `extras`

Modelo feito no Blender a partir do STL da montagem.
