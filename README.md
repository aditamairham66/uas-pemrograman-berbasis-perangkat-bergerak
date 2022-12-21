
### INSTALL IONIC CLI
npm install -g @ionic/cli

### CREATE IONIC CLI
ionic start [NAME_PROJECT] [TYPE_PROJECT] --cordova
ionic start uas2 blank --cordova

### INSTALL IONIC CORDOVA IN ANDROID
ionic cordova prepare android
ionic cordova run android -l

### INSTALL CORDOVA
npm i -g cordova

### INSTALL RUNNING NATIVE ANDROID
npm i -g native-run

### CREATE IONIC CLI
ionic start [NAME_PROJECT] [TYPE_PROJECT] --capacitor
ionic start uas2 blank --capacitor

### INSTALL IONIC CAPACITOR IN ANDROID
ionic capacitor add android
ionic capacitor copy android
ionic capacitor run android -l --external

### INSTALL IONIC CAPACITOR BUILD ANDROID
ionic capacitor build 
ionic capacitor build android
ionic capacitor build ios

npm install -g cordova-res