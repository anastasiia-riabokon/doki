```
//функції для взаємодії з локальним сховищем


//додавання даних в локальне сховище
function addDataToLocalStorage(key, value) {
  try {
    const stringifyData = JSON.stringify(value);
    localStorage.setItem(key, stringifyData);
  } catch (error) {
    console.log(error.message);
  }
}

//отримання даних зі сховища
function getDataFromLocalStorage(key) {
  try {
    const lsData = localStorage.getItem(key);
    return lsData === null ? undefined : JSON.parse(lsData);
  } catch (error) {
    console.log(error.message);
  }
}

//видалення даних зі сховища
function removeDataFromLocaleStorage(key) {
  try {
    localStorage.removeItem(key);
  } catch (error) {
    console.log(error.message);
  }
}
```