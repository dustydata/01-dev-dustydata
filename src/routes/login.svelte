<script lang='ts'>

    import { onMount } from "svelte";
    import { initializeApp } from "firebase/app";
    import { getAuth, isSignInWithEmailLink, signInWithEmailLink } from "firebase/auth";
    const firebaseConfig = {
        apiKey: "AIzaSyBymINyZcWd_0mWmz2dqPoMPI-Io65OzQs",
        authDomain: "sveltekitauth007.firebaseapp.com",
        projectId: "sveltekitauth007",
        storageBucket: "sveltekitauth007.appspot.com",
        messagingSenderId: "705326568792",
        appId: "1:705326568792:web:ac257ecca558bf1767c12d",
        measurementId: "G-E1463GMFE9"
      };
    
    const app = initializeApp(firebaseConfig);
    const auth = getAuth(app);
    onMount(async () => {
    if (isSignInWithEmailLink(auth, window.location.href)) {
      let email = window.localStorage.getItem('emailForSignIn');
      if (!email) {
        email = window.prompt('Please provide your email for confirmation');
    }
      signInWithEmailLink(auth, email, window.location.href)
  .then((result) => {
        window.localStorage.removeItem('emailForSignIn');
      })
      .catch((error) => {
      });
    }
  })
   </script>
