const express = require('express');
const app = express();
const bodyParser = require('body-parser');
const sqlite3 = require('sqlite3').verbose();
const db = new sqlite3.Database('./database.sqlite');

app.use(bodyParser.urlencoded({ extended: true }));
app.use(bodyParser.json());
app.use(express.static('public'));\napp.use('/auth', require('./auth'));\nconst bcrypt = require('bcrypt');

app.get('/', (req, res) => {
    res.sendFile(__dirname + '/index.html');
});

app.get('/catalogo', (req, res) => {
    res.sendFile(__dirname + '/catalogo.html');
});

app.get('/sobre', (req, res) => {
    res.sendFile(__dirname + '/sobre.html');
});

app.get('/contato', (req, res) => {
    res.sendFile(__dirname + '/contato.html');
});

app.get('/perfil', (req, res) => {
    res.sendFile(__dirname + '/perfil.html');
});

app.get('/admin', (req, res) => {
    res.sendFile(__dirname + '/admin.html');
});

app.listen(3000, () => {
    console.log('Servidor rodando na porta 3000');
});