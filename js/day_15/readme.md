# Difference between event.target VS this.target VS event.currentTarget

# Event Delegation

Event Delegation is basically a pattern to handle events efficiently. Instead of adding an event listener to each and every similar element, we can add an event listener to a parent element and call an event on a particular target using the .target property of the event object.

lets understand this with an example-

```
const customUI = document.createElement('ul');

for (var i = 1; i <= 10; i++) {
    const newElement = document.createElement('li');
    newElement.textContent = "This is line " + i;
    newElement.addEventListener('click', () => {
        console.log('Responding')
    })
    customUI.appendChild(newElement);
}
```

The above code will associate the function with every `<li>` element that is shown in the below image. We are creating an `<ul>` element, attaching too many `<li>` elements, and attaching an event listener with a responding function to each paragraph as we create it.

here we can make it efficient using `event delegation`. lets see an example

```
const customUI = document.createElement('ul');

function responding(evt) {
    if (evt.target.nodeName === 'li')
        console.log('Responding')
}

for (var i = 1; i <= 10; i++) {
    const newElement = document.createElement('li');
    newElement.textContent = "This is line " + i;
    customUI.appendChild(newElement);
}

customUI.addEventListener('click', responding);
```
