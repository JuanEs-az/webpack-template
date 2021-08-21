# Wepack Template
Crear aplicaciones utilizando webpack
 
### Notas:

Recordar reconstruir node_modules /
```
npm install
```
Y para reconstruir el dist /
```
npm run build
```
Iniciar el server
```
npm start
```
La carpeta assets debe de contener al menos un elemento.

Para activar el hot reload:
```javascript
index.js
...
...
if(module.hot){
    module.hot.accept()
}
```

```javascript
webpack.config.js
module.exports = {
    mode: 'development',
    devServer: {
        port: 8080,
        static: path.resolve(__dirname, 'dist'),
        hot: true, <---
        liveReload: true
    },
    ...
}
```