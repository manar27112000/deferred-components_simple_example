# Deferred Component Example in Flutter

This is a simple Flutter task demonstrating **Deferred Components**,
a feature that allows you to load parts of your app only when needed instead of loading everything at startup.

---

## Concept

- **Deferred Component:** A widget or module that is **not loaded initially**. It is only loaded when the user requests it.  
- **Why use it?** Helps reduce app startup time and initial memory usage, especially if you have heavy widgets or assets.
   
- **How it works in Flutter:** 
  1. Import the Dart file as **deferred**
  2. Import 'box.dart' deferred as box;
  3. Load it on demand using:
     
     await box.loadLibrary();
     
 4. Then use the widget as usual:
    
     const box.DeferredBox()
    

## How This Project Works

1. The app starts with a **button** labeled "Load Box".  
2. When the button is pressed:
   - The `box.dart` file is loaded using `loadLibrary()`.  
   - A **loading indicator** (`CircularProgressIndicator`) appears while loading.  
3. After loading completes, the **DeferredBox** widget is displayed.  
4. The box is a simple **100x100 blue container** with the text "Loaded!".

---

## Usage

1. Run the app.
2. Press **"Load Box"**.
3. Observe the loading indicator, then see the box appear.

---

## Key Takeaways

- Deferred Components reduce **initial app size** and improve **performance**.  
- Useful for loading **heavy widgets, images, or modules** only when needed.  
- Easy to implement using **`deferred as`** imports and **`loadLibrary()`**.

