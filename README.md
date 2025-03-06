# MERN Stack Interview Questions & Answers

## 🖊 JavaScript Questions & Answers

### **Basic JavaScript Answers**

1. **JavaScript kya hai?**\
   JavaScript ek **high-level, interpreted** programming language hai jo web pages ko interactive banane ke liye use hoti hai. Ye **client-side aur server-side** dono pe use ho sakti hai.

2. `var`**, **`let`*, aur **`const`** me difference:**

   - `var`: Function-scoped hota hai, hoisting hoti hai.
   - `let`: Block-scoped hota hai, hoisting hoti hai but initialized nahi hota.
   - `const`: Block-scoped hota hai, hoisting hoti hai but reassigned nahi ho sakta.

3. **Hoisting kya hoti hai?**\
   JavaScript me **variables aur functions** ko execution se pehle memory me allocate kar diya jata hai. Is process ko **hoisting** kehte hain.

4. **Closures kya hote hain?**\
   Jab ek function dusre function ke andar declared hota hai aur andar wala function **bahar wale function ki variables ko access** kar sakta hai, toh ise closure kehte hain.

   ```js
   function outer() {
       let count = 0;
       return function inner() {
           count++;
           console.log(count);
       }
   }
   const counter = outer();
   counter(); // 1
   counter(); // 2
   ```

5. ``** aur **``** me difference:**

   - `==` (Loose Equality): Type conversion karta hai. (`5 == "5"` → `true`)
   - `===` (Strict Equality): Type conversion nahi karta. (`5 === "5"` → `false`)

6. **Higher Order Function:**\
   Jo function **ek ya ek se zyada functions ko argument me leta hai ya function return karta hai**, use higher-order function kehte hain.

7. **Callback function kya hota hai?**\
   Jab ek function **dusre function ko argument me pass** kiya jata hai aur wo function **baad me execute** hota hai, use callback function kehte hain.

8. **Event Loop kaise kaam karta hai?**\
   JavaScript **single-threaded** hoti hai, lekin event loop ki help se asynchronous tasks ko efficiently execute karti hai.

9. **Promise aur Async/Await difference:**

   - Promise `.then()` aur `.catch()` ke saath kaam karta hai.
   - Async/Await code ko **synchronous jaisa likhne** ki suvidha deta hai.

---

## ⚛ React.js Questions & Answers

1. **React kya hai?**\
   React ek **JavaScript library** hai jo UI components banane ke liye use hoti hai.

2. **State aur Props me difference:**

   - **State:** Component ke andar ka data hota hai jo change ho sakta hai.
   - **Props:** Parent component se data receive karne ka tarika hai. Immutable hota hai.

3. **useEffect() ka use kya hai?**

   - useEffect **side effects** handle karne ke liye use hota hai, jaise API calls, event listeners, etc.

   ```js
   useEffect(() => {
       console.log("Component Mounted");
   }, []);
   ```

4. **Redux kya hai?**\
   Redux ek **state management library** hai jo **global state** manage karne me help karti hai.

---

## 🛠 Node.js & Express.js Questions & Answers

1. **Node.js kya hai?**\
   Node.js ek **JavaScript runtime environment** hai jo **non-blocking, event-driven architecture** follow karta hai.

2. **Middleware kya hota hai?**\
   Middleware functions **request aur response ke beech me execute** hote hain.

   ```js
   app.use((req, res, next) => {
       console.log("Middleware executed");
       next();
   });
   ```

3. **REST API kaise banate hain Express.js me?**

   ```js
   app.get("/users", (req, res) => {
       res.json([{ name: "John" }]);
   });
   ```

---

## 🕥 MongoDB Questions & Answers

1. **MongoDB kya hai?**\
   MongoDB ek **NoSQL database** hai jo **JSON-like documents** store karta hai.

2. **Mongoose kya hai?**\
   Mongoose ek **ODM (Object Data Modeling)** library hai jo MongoDB ke sath kaam karti hai.

   ```js
   const UserSchema = new mongoose.Schema({ name: String });
   const User = mongoose.model("User", UserSchema);
   ```

---

## 🔒 Security & Deployment Questions & Answers

1. **JWT Authentication kaise implement karte hain?**

   ```js
   const token = jwt.sign({ userId: 123 }, "SECRET_KEY", { expiresIn: "1h" });
   ```

2. **CSRF aur XSS attack se kaise bacha jata hai?**

   - CSRF se bachne ke liye **CSRF tokens** ka use karein.
   - XSS se bachne ke liye **input sanitization** karein.

---

## 📄 Coding Questions & Answers

1. **Reverse a string without built-in function:**

   ```js
   function reverseString(str) {
       let reversed = "";
       for (let i = str.length - 1; i >= 0; i--) {
           reversed += str[i];
       }
       return reversed;
   }
   console.log(reverseString("hello")); // "olleh"
   ```

2. **Find missing number in array:**

   ```js
   function findMissingNumber(arr, n) {
       let expectedSum = (n * (n + 1)) / 2;
       let actualSum = arr.reduce((sum, num) => sum + num, 0);
       return expectedSum - actualSum;
   }
   console.log(findMissingNumber([1, 2, 4, 5, 6], 6)); // 3
   ```

3. **Check palindrome string:**

   ```js
   function isPalindrome(str) {
       return str === str.split("").reverse().join("");
   }
   console.log(isPalindrome("madam")); // true
   ```

---

Yeh **MERN Stack interview** ke sabse important questions aur answers hain. Agar tumhe aur details chahiye ya kisi aur topic par clarity chahiye, toh batao! 🚀

