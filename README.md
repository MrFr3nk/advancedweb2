

<!DOCTYPE html>

<html>

<head>

  <title>Falling Star Effect</title>

  <style>

    body {

      background-color: black;

      overflow: hidden;

    }

    

    .star {

      position: absolute;

      width: 2px;

      height: 2px;

      background-color: white;

      animation: fallingStar 2s linear infinite;

    }

    

    @keyframes fallingStar {

      0% {

        top: -10px;

        opacity: 1;

      }

      100% {

        top: 100%;

        opacity: 0;

      }

    }

    

    .text {

      position: absolute;

      top: 50%;

      left: 50%;

      transform: translate(-50%, -50%);

      font-size: 24px;

      color: white;

      text-transform: uppercase;

      font-family: Arial, sans-serif;

      animation: glowingText 2s ease-in-out infinite;

    }

    

    @keyframes glowingText {

      0% {

        text-shadow: 0 0 10px white;

      }

      50% {

        text-shadow: 0 0 20px white;

      }

      100% {

        text-shadow: 0 0 10px white;

      }

    }

  </style>

</head>

<body>

  <div class="text">You message has been submitted !</br></br>Thank you for visiting our website have a nice day<br><br><center>

  	<marquee behavior="alternate" scrollamount="7">

  <point><font color="#ff003333"> <p>Darrell Mucheri</p></font></point>

  </marquee>   

  </center></div>

  

  

 



  <script>

    function createStar() {

      const star = document.createElement('div');

      star.classList.add('star');

      star.style.left = Math.random() * window.innerWidth + 'px';

      document.body.appendChild(star);

      

      setTimeout(() => {

        star.remove();

      }, 2000);

    }

    

    setInterval(createStar, 200);

  </script>

</body>

</html>

```

