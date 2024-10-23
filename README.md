npm install reactstrap
npm install --save bootstrap


LINKS
https://reactstrap.github.io/?path=/docs/home-installation--page

https://www.npmjs.com/package/@elbrus/create-config
npm init @elbrus/config@latest


Связи
https://github.com/Elbrus-Bootcamp/sequelize-relations-example


Шифрование, пример:
npm install bcrypt

const bcrypt = require('bcrypt');

// Хеширование пароля
const saltRounds = 10; // Количество раундов генерации соли
const myPlaintextPassword = 'mySecretPassword';

bcrypt.hash(myPlaintextPassword, saltRounds, function(err, hash) {
    if (err) {
        console.error(err);
        return;
    }

    console.log('Hashed password:', hash);

    // Проверка пароля
    bcrypt.compare(myPlaintextPassword, hash, function(err, result) {
        if (err) {
            console.error(err);
            return;
        }

        if (result) {
            console.log('Password matches');
        } else {
            console.log('Password does not match');
        }
    });
});

AXIOS
Автоматическое преобразование: Axios автоматически преобразует данные ответа JSON.

Axios автоматически парсит содержимое JSON и возвращает свойство response.data как уже готовый JavaScript объект, который можно использовать непосредственно в коде.

npm install axios

Пример на промисах:

axios.get('https://api.example.com/data')
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error(error);
  });


axios.post('https://api.example.com/data', {
    firstName: 'Masha',
    lastName: 'AI'
  })
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error(error);
  });

Пример на асунке:

const axios = require('axios');

async function fetchData() {
  try {
    const response = await axios.get('https://api.example.com/data');
    console.log(response.data);
  } catch (error) {
    console.error(error);
  }
}

fetchData();


async function sendData() {
  try {
    const response = await axios.post('https://api.example.com/data', {
      firstName: 'Masha',
      lastName: 'AI',
    });
    console.log(response.data);
  } catch (error) {
    console.error(error);
  }
}

sendData();


