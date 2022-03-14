```javascript

// at runtime

// we pass a reference to a function
<li onClick={() => handleNoteSelection(note.id)}>{note.title}</li>

// we pass the result of the function (expression)
// at runtime, this is undefined
<li onClick={handleNoteSelection(note.id)}>{note.title}</li>

// this will also work, however, we are not able to pass the node id
<li onClick={handleNoteSelection}>{note.title}</li>
```

# What is an expression?
An expression always returns a value (even if that value is `undefined`)

# Array methods you should be familiar with;

- Array.find()
- Array.filter()
- Array.splice()
- Array.map()
- Array.forEach()
- Array.sort()
- (optionally) Array.reduce()

# Legibility is more important than brevity

Being able to read the code is more important than having short code

[Clean code with Uncle Bob](https://www.youtube.com/watch?v=Wibk0IfjfaI)
