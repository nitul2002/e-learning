# E-Learning platform for online courses.

New project's website (under construction): [Realtime E-Learning](https://e-learning-7c6ae.firebaseapp.com/)

## Getting Started

You need a Unix PC to clone this webapp!

- Install Node.js >= 7.4.0 [https://nodejs.org/](https://nodejs.org/)

- Install a Git client. I recommend SourceTree [https://www.sourcetreeapp.com/](https://www.sourcetreeapp.com/)

- Clone this repository into a folder in your computer [https://help.github.com/articles/which-remote-url-should-i-use/](https://help.github.com/articles/which-remote-url-should-i-use/)

- Install the dependencies using NPM or Yarn:

````
npm install
````

- Create a new project in your [Firebase account](http://firebase.google.com)

- Enable at the Email/Password provider in the [Firebase authentication providers](https://console.firebase.google.com/project/bigmomo-647f1/authentication/providers)

- Create a file called `.env` in the root of your cloned repository and add the following code. Replace the values with the ones from the project you created in Firebase:

````
FIREBASE_API_KEY=your_firebase_api_key
FIREBASE_AUTH_DOMAIN=your_firebase_project.firebaseapp.com
FIREBASE_DATABASE_URL=https://your_firebase_project.firebaseio.com
FIREBASE_STORAGE_BUCKET=your_firebase_project.appspot.com
````

- Update the default project value in `.firebaserc`

- If you want some demo data, import `/data/demo-data.json` into your Firebase database

- If you are going to use Firebase storage, you should give read access to everyone, otherwise only the authenticated users will be able to download images or files. In your [Firebase console](https://console.firebase.google.com), replace the rules with these ones:

````
allow read: if true;
allow write: if request.auth != null;
````

- To give a user admin rights, you have to add a field called `level` with the value `5` into a user (using the firebase UI). Once you do that, login into Nekomy with that user and you will see the `admin` link in the sidebar navigation

### Start development server with hot reloading

````
npm run dev
````

### Testing

Run test once

````
npm run test
````

Test watch

````
npm run test:watch
````

### Linting

Linting is using Airbnb Eslint configuration

````
npm run lint
````

### Deploy to production

Build for production

````
npm run build
````

Install Firebase tools (if you haven't done it yet)

````
npm install -g firebase-tools
````

Login and init the project

````
firebase login
firebase init
````

Deploy to Firebase

````
firebase deploy
````

## Contributor License Agreement

By contributing your code to Nekomy you grant to the repository owner a non-exclusive, irrevocable, worldwide, royalty-free, sublicenseable, transferable license under all of Your relevant intellectual property rights (including copyright, patent, and any other rights), to use, copy, prepare derivative works of, distribute and publicly perform and display the Contributions on any licensing terms, including without limitation: (a) open source licenses like the MIT license; and (b) binary, proprietary, or commercial licenses. Except for the licenses granted herein, You reserve all right, title, and interest in and to the Contribution.

You confirm that you are able to grant us these rights. You represent that You are legally entitled to grant the above license. If Your employer has rights to intellectual property that You create, You represent that You have received permission to make the Contributions on behalf of that employer, or that Your employer has waived such rights for the Contributions.

You represent that the Contributions are Your original works of authorship, and to Your knowledge, no other person claims, or has the right to claim, any right in any invention or patent related to the Contributions. You also represent that You are not legally obligated, whether by entering into an agreement or otherwise, in any way that conflicts with the terms of this license.

The repository owner acknowledges that, except as explicitly described in this Agreement, any Contribution which you provide is on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING, WITHOUT LIMITATION, ANY WARRANTIES OR CONDITIONS OF TITLE, NON-INFRINGEMENT, MERCHANTABILITY, OR FITNESS FOR A PARTICULAR PURPOSE.

## Credits

Icons from Flaticon.com (Freepik and Madebyoliver), triangles background by rvika from Fotolia and photos from Google Creative Commons search results
