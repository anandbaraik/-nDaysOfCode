# Map

Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type. Map object can hold both objects and primitive values as either key or value

# Creating an empty Map

```
const map = new Map()
console.log(map) //Map(0) {size: 0}
```

# Creating an Map from array

```
countries = [
  ['Finland', 'Helsinki'],
  ['Sweden', 'Stockholm'],
  ['Norway', 'Oslo'],
]
const map = new Map(countries)
console.log(map)
console.log(map.size)
<!-- Map(3) {"Finland" => "Helsinki", "Sweden" => "Stockholm", "Norway" => "Oslo"}
3 -->
```

# Adding values to the Map

```
const countriesMap = new Map()
console.log(countriesMap.size) // 0
countriesMap.set('Finland', 'Helsinki')
countriesMap.set('Sweden', 'Stockholm')
countriesMap.set('Norway', 'Oslo')
console.log(countriesMap)
console.log(countriesMap.size)
<!-- Map(3) {"Finland" => "Helsinki", "Sweden" => "Stockholm", "Norway" => "Oslo"}
3 -->
```

# Getting a value from Map

```
console.log(countriesMap.get('Finland')) //Helsinki
```

# Checking key in Map

Check if a key exists in a map using `has` method. It returns true or false.

```
console.log(countriesMap.has('Finland')) //true
console.log(countriesMap.has('Morroco')) //false
```

Getting all values from map using loop

```
for (const country of countriesMap) {
  console.log(country)
}

<!-- (2) ["Finland", "Helsinki"]
(2) ["Sweden", "Stockholm"]
(2) ["Norway", "Oslo"] -->
```

```
for (const [country, city] of countriesMap){
 console.log(country, city)
}
<!-- Finland Helsinki
Sweden Stockholm
Norway Oslo -->
```

# Removes the elements by key

Syntax

```
map.delete(key)
```

# Remove all element at once

Syntax

```
map.clear()
```
