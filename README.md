# guessing-game
#! /usr/bin/env node

import inquirer from "inquirer";
// computer will generate a random number - Done

// user input for guessing number - Done

//compare user input with computer generated number and show result

const randomNumber = Math.floor(Math.random() * 10 + 1);
console.log("welcome to game");

const answer = await inquirer.prompt([
    {
        name: "userGuessedNumber",
        type: "number",
        message: "Please guess a number between 1-10: ",
    },
]);
if (answer.userGuessedNumber === randomNumber) {
    console.log("Congractulation! you guess right number ");
}
else {
    console.log("you guess wrong number");
}