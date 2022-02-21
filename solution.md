1. Your main method should look like this:

```dart
void main() {
}
```

2. Create your function, name it `deleteVowels` and it will return a `string` and accept a `string`:

```dart
void main() {
  String deleteVowels(String text){
  }
}
```

3. The first step is to create a list with the vowels:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
  }
}
```

4. Create a variable called `result` to store our characters that are not vowels:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
    String result = "";
  }
}
```

5. Iterate over the `text` argument, but it's not iterable.., we can use the `split` method to turn `text` to a list of characters:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
    String result = "";
    for(String character in text.split('')){
    }
  }
}
```

6. Now check vowels contains this character using the `contains` method:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
    String result = "";
    for(String character in text.split('')){
      if(vowels.contains(character)){
      }
  }
}
```

7. We want the character if it's **not** contained within the vowels list, so add `!` to reverse the condition:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
    String result = "";
    for(String character in text.split('')){
      if(!vowels.contains(character)){
      }
  }
}
```

8. The list is in `uppercase` and the `text` argument may be upper or lower case, to solve this let's use `toUpperCase` method:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
    String result = "";
    for(String character in text.split('')){
      if(!vowels.contains(character.toUpperCase())){
      }
  }
}
```

9. Now add this `character` to the `result` variable and return the `result` after we finish `iterating`:

```dart
void main() {
  String deleteVowels(String text){
    const vowels = ['A','E','O','I','U'];
    String result = "";
    for(String character in text.split('')){
      if(!vowels.contains(character.toUpperCase())){
          result += character
      }
  }
  return result;
}
```
