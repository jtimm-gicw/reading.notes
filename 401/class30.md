# 401-Read_30
# 🗂️ Hashtables - Study Notes

## 📌 What is a Hashtable?
- A **data structure** that stores data as **key → value pairs**.  
- Super fast lookups using a **hash function**.  
- Lookup time: **O(1)** (constant time) ⚡ (ideal for quick searches).

---

## 📖 Key Terminology
- 🔑 **Hash** → A number created by running a key through a hash function (decides array index).  
- 🪣 **Bucket** → Each index in the array; can store **one or multiple key/value pairs**.  
- 💥 **Collision** → When two different keys hash to the same bucket/index.

---

## 🎯 Why use Hashtables?
- ✅ Store **unique values**  
- ✅ Work like a **dictionary** (word → definition)  
- ✅ Used in **libraries**, **databases**, and **caches**  

---

## ⚙️ How Hashtables Work
1. Accept a **key**.  
2. Run it through a **hash function** → get a number.  
3. Use `modulus (%)` to fit it into the array size.  
4. Store the **key & value** in the correct bucket.  

👉 To **get** a value:  
- Run the key through the same hash function, find the bucket, and search for the key/value pair.

---

## 🧩 Example
Seattle neighborhoods & zip codes:  
```js
hashMap.add("Greenwood", 98103);
hashMap.add("Downtown", 98101);
