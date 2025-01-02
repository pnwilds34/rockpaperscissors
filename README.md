# rockpaperscissors
Rock Paper Scissors project in Java - 


const getUserChoice = (userInput) => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock' || userInput === 'paper' || userInput === 'scissors') {
    return userInput 
  } else {
    console.log('Error. Please choose rock,paper or scissors.');
  }
}

const getComputerChoice = () => {
  const randomNumber = Math.floor(Math.random()* 3);
  switch (randomNumber) {
    case 0:
      return 'rock';
    case 1:
      return 'paper';
    case 2:
      return 'scissors';
  }
};

//Determining the Winner
const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice) {
    return 'Its a tie!';
  }

  if (userChoice === 'rock') {
    if (computerChoice === 'paper') {
      return 'Computer won.';
    } else {
      return 'You won!';
    }
  }

if (userChoice === 'paper') {
  if (computerChoice === 'scissors') {
      return 'Computer won.';
    } else {
    return 'You Won!';
    }
  }

if (userChoice === 'scissors') {
  if (computerChoice === 'rock') {
    return 'Computer won!';
  } else {
    return 'You won!';
  }
}

};

const playGame = () => {
    const userChoice = getUserChoice('paper');
    const computerChoice = getComputerChoice(); 
    console.log(`You chose: ${userChoice}.`);
    console.log(`Computer chose: ${computerChoice}.`);
    
    console.log(determineWinner(userChoice, computerChoice));
};

playGame();
