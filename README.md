## How to stup Tailwind CSS

Step 1: Run the following commands

```
npm init
npm install -D tailwindcss
npx tailwindcss init  
```

Step 2: Update ``tailwind.conf.js`` file to include this line: 
```
content: ["./index.html","./src/**/*.{html,js}"],
```  
It'll include your all html & js file even if it's in the folder named src

Step 3: Create src/input.css to include  
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```  

Step 4: Run the following command:
```
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```  
Now it will start to build.  

If you don't want to run the step 4 command you easily copy this command and go to ``package.json`` file and paste inside the scripts.  
```
"build" : "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch",
```  
So it will create a script name called build. Then you just need to run this following command : 
```
npm run build
```  

After that it will start to build and you are good to go.  

Step 5: In the final step you have to create a html file and link up the output file  
```
<link rel="stylesheet" href="./dist/output.css">
```

---

#### Note that you can name your files and folders whatever you want

