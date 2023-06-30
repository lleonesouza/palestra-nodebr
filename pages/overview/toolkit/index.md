---
layout: two-cols
---


<h2>Toolkit</h2>
  <p>Experiência de desenvolvimento com NodeMCU</p>
  <ul>
    <li>Encontra dispositivos conectados</li>
    <li>Faz upload e delete de código</li>
    <li>Acesso ao terminal</li>
    <li>Libs de sensores em Lua</li>
    <li>Exemplos de projetos</li>

  </ul>

  <div>
    <img src="pages/overview/toolkit/imgs/github.png" />
    <button>https://github.com/lleonesouza/toolkit-mcu</button>
  </div>

::right::
  <!-- <h2>Módulos Disponiveis:</h2>
  <br/>
  <ul>
    <li>DHT11</li>
    <li>ds18b20</li>
    <li>MH-Series</li>
    <li>Motor</li>
    <li>MQ-135</li>
    <li>Relay</li>
    <li>Sonar</li>
  </ul> -->

<style>
img {
        width: 200px
}
</style>



---
layout: image-right
image: pages/overview/toolkit/imgs/devices.gif
---
# Devices

to run:

```
yarn devices
npm run devices
```


Busca todos devices conectados.



---
layout: image-right
image: pages/overview/toolkit/imgs/upload.gif
---

# Upload

Upload project in nodemcu

to run:

```
yarn upload
npm run upload
```


Faz **upload** dos arquivos na pasta 'project' para o nodemcu.

---
layout: image-right
image: pages/overview/toolkit/imgs/mkfs.gif
---

# Mkfs

Format the file system
to run:

```
yarn mkfs
npm run mkfs
```

Deleta os arquivos do Nodemcu.

---
layout: image-right
image: pages/overview/toolkit/imgs/terminal.gif
---
# Terminal

Get a terminal in nodemcu
to run:

```
yarn terminal
npm run terminal
```

Abre um terminal no Nodemcu para executar comandos.



