# Firebase2 - Cookbook
  Firebase settings 

- Index
  + How to Install
  + Install Packages



### How to Install

```
  npm i firebase angularfire2 --save
```
##### index.html 
ps: See in the firebase ( WEB )
```
  <script src="https://www.gstatic.com/firebasejs/3.6.7/firebase.js"></script>
``` 



##### app.module.ts
```
  // firebase 
  import { AngularFireModule } from 'angularfire2';
  import { firebaseConfig } from './environments/firebaseconfig';
  declare var firebase: any;
  
  imports: [  AngularFireModule.initializeApp( firebaseConfig ) ] 
```

##### environments/firebaseconfig.ts
```

 export const firebaseConfig = {
     apiKey: " xxxxxxxxxxxxxxx ",
     authDomain: " xxxxxxxxxxxxxxxxxxx ",
     databaseURL: " xxxxxxxxxxxxxxxxxx  ",
     storageBucket: " xxxxxxxxxxxxxxxx ",
     messagingSenderId: " xxxxxxxxxxx "
   };
     firebase.initializeApp(firebaseConfig);

```


### How to Deploy

First install the firebase-tools
```
sudo npm i -g firebase-tools
``` 

With --prod flag ( minify + uglify ) the application
```
ng build --prod
```

```
ng build --env=prod
``` 

```
firebase login
```

```
firebase init 
> dist
> y
> y
// or overwrite ? N
``` 

#### need help
```
firebase deploy --help
``` 




