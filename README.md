# Utils
Funções úteis para não esquecer!

## Tabela de conteúdos
<!--ts-->
   * [React](#react)
<!--te-->

## React
### Converter dados em JSON e fazer download
```
var htmlElement = document.createElement("a");
var stringJson = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(meusDadosParaConverterEmJson));
htmlElement.setAttribute("href", stringJson);
htmlElement.setAttribute("download", "meusDadosConvertidos.json");
document.body.appendChild(htmlElement);
htmlElement.click();
document.body.removeChild(htmlElement);
```
### Converter url de uma imagem em base64 
```
function converterImagemEmBase64(urlDaImagemParaConverter, callbackRetornandoOBase65) {
  var img = new Image();
  img.crossOrigin = "Anonymous";
  img.onload = function () {
    var canvas = document.createElement("CANVAS"),
      ctx = canvas.getContext("2d"),
      dataURL;
    canvas.height = img.height;
    canvas.width = img.width;
    ctx.drawImage(img, 0, 0);
    dataURL = canvas.toDataURL(`image/png`);
    callbackRetornandoOBase65(dataURL);
    canvas = null;
  };
  img.src = urlDaImagemParaConverter;
}
```
