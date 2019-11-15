# random-password-generator

This password generator creates a completely (pseudo)random password based on user-selected criteria of legnth and character-type. It runs in the browser and has a dynamic design suited for mobile or desktop. 

Live page link: https://mattbeachey.github.io/random-password-generator/

This is the first app I've built entirely by myself in Javascript. It required me to synthesize several discrete skills and methods I've learned into designing an app to achieve a single goal.

Because the criteria calls for a user to be able to select from four categories of character-type, I had to generate a function that would combine only the character-arrays with the called-for characters. However, simply selecting random characters from a combined array would not guarentee that the final password contained at least one of each original character type. To ensure that at least one of each character-type ended up in the final generated password, I had to also design the function to put a single character from the selected array into the final password, and then also pass along all characters from the selected array into a combined array, from which the remaining characters would be randomly selected.

Finally, the function scrambles the final password after generating it to the user's desired length. This is not something I'm familiar doing in JavaScript, so I referenced the following funciton from https://medium.com/@nitinpatel_20236/how-to-shuffle-correctly-shuffle-an-array-in-javascript-15ea3f84bfb:
         
          for (let i = finalPasswordArray.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * i)
            const temp = finalPasswordArray[i]
            finalPasswordArray[i] = finalPasswordArray[j]
            finalPasswordArray[j] = temp
          }

Planned features:
I intended to add a functional "copy to clipboard" button, but I couldn't quite get that js working. I will update that soon, however.

