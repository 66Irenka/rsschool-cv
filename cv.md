# Iryna Pavlenko

=======

## Contacts.

- Github: https://github.com/66Irenka
- Discord: irynapavl91 (@irynapavl91)

## About me.

I'm very creative persone. I want improve my developing skills with yout school.

## Skills.

- HTML
- CSS
- JavaScript (basics)
- GitHub

## Code Example.

```javascript
const options = {
  method: "GET",
};

const url = "https://api.thecatapi.com/v1/images/search";
const section = document.querySelector(".container");
const button = document.querySelector(".btn");
const tagInput = document.getElementById("tagInput");
const tagCheckbox = document.getElementById("tagCheckbox");

button.addEventListener("click", function () {
  const tag = tagInput.value.trim();
  getRandomCats(tag);
});

tagCheckbox.addEventListener("change", function () {
  tagInput.disabled = !tagCheckbox.checked;
});

// We getting the first cat image when the page loads

window.onload = function () {
  getRandomCats();
};

function randomCatPhoto(json) {
  let photo = json[0].url;
  section.classList.add("cats");

  let image = document.createElement("img");
  image.src = photo;
  image.classList.add("random_cats");
  image.alt = photo;
  section.appendChild(image);
}

async function getRandomCats(tag) {
  section.innerHTML = "";

  let apiUrl = "https://api.thecatapi.com/v1/images/search";

  if (tag) {
    apiUrl += `?tag=${tag}`;
  }

  try {
    const response = await fetch(apiUrl, options);
    const json = await response.json();
    console.log("JSON:", json);
    return randomCatPhoto(json);
  } catch (e) {
    console.log("Це помилка");
    console.log(e);
  }
}
```

## Experience.

I don't have real practice yet

## Education.

University: Uman National University of Horticulture
Master's degree
The Faculty of Management
Courses: Course of Frontend 2023-2024 with mentor

## English.

I have an intermediate level of English, I practice speaking with a native speaker from the USA
