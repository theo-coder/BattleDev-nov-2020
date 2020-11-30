<p align="center">
    <img src="https://www.shareicon.net/data/512x512/2015/11/09/669182_terminal_512x512.png" width="50px">
</p>
<h1 align="center">BattleDev HelloWork - 26 novembre 2020</h1>

<div align="center">

[![NodeJS](https://img.shields.io/badge/nodejs-v14.13.1-009D28.svg?style=for-the-badge&logo=node.js)](https://nodejs.org/)
[![BattleDev](https://img.shields.io/badge/battledev-26.11.2020-000000.svg?style=for-the-badge&logo=buddy)](https://battledev.blogdumoderateur.com/)

</div>

---

## 📝 Table des matières

- [📝 Table des matières](#-table-des-matières)
- [📚 Présentation du projet <a name = "description"></a>](#-présentation-du-projet-)
- [📜 Exercice 1 <a name="ex1"></a>](#-exercice-1-)
- [📜 Exercice 2 <a name="ex2"></a>](#-exercice-2-)
- [👨‍👦‍👦 Liste des participants <a name="credits"></a>](#-liste-des-participants-)

## 📚 Présentation du projet <a name = "description"></a>

Liste de nos travaux pour la BattleDev du 26 novembre 2020 en langage NodeJS

## 📜 Exercice 1 <a name="ex1"></a>

L'exercice 1 consistait à vérifier le nombre de comptes followers de Dolan Grump considérés comme suspect. Pour qu'un compte soit suspect il fallait que les 5 derniers caractères de son nom soient des nombres. Pour ceci l'approche à été de boucler sur l'ensembles des chaines d'entrée puis sur chacun des 5 derniers caractères pour vérifier leur type. Ainsi le résultat était le nombre de comptes suspect.

```js
function ContestResponse(){
    // Le premier input correspondant au nombre de comptes à vérifier
    let n = input[0];
    // La variable qui servira à la réponse
    let res = 0;
    // Boucle sur l'ensemble des comptes
    for(let i=1;i<=n;i++){
        // La variable qui compte la quantité de nombre dans les 5 derniers caractères
        let count = 0;
        // Boucle sur les 5 derniers caractères
        for(let j=input[i].length; j >= input[i].length-5; j--){
            // Vérification du type
            Number.isInteger(parseInt(input[i][j])) && count++
        }
    // Vérification de la quantité de nombres
    count === 5 && res++
  }
  // Affichage de la réponse
  console.log(res)
}
```

## 📜 Exercice 2 <a name="ex2"></a>

Après, dans l'exercice 1 avoir analyser les comptes suspects, il fallait se pencher sur les tweets. L'entrée nous donnait plusieurs heures de posts. Si la quantité de posts était supérieure la nuit, alors le compte était considéré comme suspect, et ainsi il fallait renvoyer la chaine 'SUSPICIOUS' sinon il fallait renvoyer la chaine 'OK'. Pour cela Il fallait simplement vérifier si l'heure de post était supérieure ou égale à 20 ou strictement inférieure à 8. Et ainsi vérifier que plus de la moitié des posts étaient postés la nuit.

```js
function ContestResponse(){
    // Initialise le compteur
    let count = 0
    // Boucle sur les entrées
    for(let i=1; i<input[0]; i++){
        // Assigne les heures à h et les minutes à m
        let [h, m] = input[i].split(':')
        // Vérifie si les heures sont comprises entre 8 et 19 et ajoute 1 au compteur
        if((h >= 20) || (h < 8)) { count++ }
    }
    // Vérifie si le compteur est supérieur à la moitié du nombre d'entrées et affiche le résultat
    count > (input[0]/2) ? console.log('SUSPICIOUS') : console.log("OK")
}
```

## 👨‍👦‍👦 Liste des participants <a name="credits"></a>

[![TheoCoder](https://img.shields.io/badge/theocoder-visit-blue.svg?style=for-the-badge&logo=data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCAAZABkDASIAAhEBAxEB/8QAGQAAAgMBAAAAAAAAAAAAAAAABQYAAgQI/8QAKxAAAQMDAwIDCQAAAAAAAAAAAQIDBAAFERIhMQZREzKBFCNBQmFxkaGx/8QAGAEAAwEBAAAAAAAAAAAAAAAAAQIDBAf/xAAeEQACAwACAwEAAAAAAAAAAAABAgADEQQhE0GBkf/aAAwDAQACEQMRAD8A4G6fsKr7JLZfRFaSQFPOAkAk4A237n0NbD05bPbA2OpoBY05L3gv89tPh5rfY06E2cxd8FbyBxrlJ8qVdsDGO9alNMwL/aHZMWJIcTbH332kx20tqdSJBAKAnScaUjj5a63XxiUDDPv7GRNEXuoem1WLwVoktTY7oBS8z5dwFD7ZBB335yARQX0/VOt0fVOM0zEobzCaVIS0gIQ06kBLYSkbA4AGkYHNJeaycirxtkmRhhewXtFpcUl9kvsEhwJB3QscKGfWisXqu2RZkN4W991cdhxguvPBRUFlwk6QAM+8I5x9M0qVKVbmChT6gDZ1Ct2uzUpgMRg6ELcLzy3iNTiz3x8AP7Qn81O1XqT2NYdMBO9z/9k=)](https://github.com/theo-coder)
[![Theomi](https://img.shields.io/badge/theomi-visit-blue.svg?style=for-the-badge&logo=data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCAAZABkDASIAAhEBAxEB/8QAGQAAAgMBAAAAAAAAAAAAAAAABwgBBQYJ/8QAKxAAAQMDAgQGAgMAAAAAAAAAAQIDBAUGEQASBwghURQVIjEyQRhhI0Oh/8QAFwEAAwEAAAAAAAAAAAAAAAAAAwQFAv/EABsRAQACAwEBAAAAAAAAAAAAAAIBAwAEMRES/9oADAMBAAIRAxEAPwDoFzBcbGOA/CG4L3ep7lXNNQ2GoLKglTzjjqGkDPbcsE9CcA6Qz89OPM2reYOUCbSqW8Q4zDNtOBATn47lBSljBB3BQzg+3TTT82kIXFwxhMK3FDNagyVdAUkJdHRWT7HP70I6PfN1w7YuBcijvo8A44xGS7BUhx/Z0K22wsl1Bz6cY3YOCcg6l7Wwq38nKupQLD9LGA5VeZgcxFm1KZLphpFco8sQp8bYpCCopCkrSlXqSCD8VZIIPU6Nnjh30pXKWzM87vK4Z7L0SVVYtMC47scsFspS+5hSdysLAfSFJySNvXtpjvMv3p2ly64U9xG4QLJMcwf3jRWLytybSZKtgfR/G7gKLTgOULA7hQB0CaxSbybnw479MmPSoxCEqhNqWw9g5SQsKCQCR/Z7dtH4++pOsXawv8ldwlGy6PYPMo+GtvyLUobpnrbXVZzxlSy0fSlRAAQD9hKQBn7OT961njj3/wB1XD61OjgwDBPIxdqWpS7Of//Z)](https://github.com/theomi)
[![TeissierYannis](https://img.shields.io/badge/teissieryannis-visit-blue.svg?style=for-the-badge&logo=data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCAAZABkDASIAAhEBAxEB/8QAGQAAAgMBAAAAAAAAAAAAAAAACAkEBgcF/8QAMRAAAQIEBAQDBwUAAAAAAAAAAQIDBAUGEQAIEiEHEyIxFjZSFBUyM0FxkkJhdLLB/8QAFwEBAQEBAAAAAAAAAAAAAAAABQIDBP/EACERAAICAgEEAwAAAAAAAAAAAAECAAMREyEEEjHwQVGR/9oADAMBAAIRAxEAPwBoLFRymJeLLUzg3XQEnQh9JNiLg2v9RvhXmevjZGzLMqaXk9LWRy2pc9GdfNiz35oABBSAqwNiSE99rCp1bmHjKWoCLnb0npuXlCQ0wxCy9BdfcKUp7ulYNki527JtiLEZr6KqThjFzeYy2Pkca20YOCXCuMGNhlJGhBbWNKlKK9RvpP6jsBbBl776QUQsCcePfuJdLWq2MLGAIGffyE9SHCtinprSsMpsJ9jpuPJ2+qohQ/3HZ8KNelOMRyV5kp5xrkM48VPNRk8p+Wqg1RrTQQX2nHUqQtYAAC78wGwA6R++N79+Q/qP4nB19JpbWw5EuuzYO4fMB6tMm9d8QqWo+bRDjUtg1rdL0uiFKS8lshGlRFiAo2PSbEAC9jsKAvIdV8CXHDN4RNnm3ggslaSUAjfqHe+Gl1J5dh/vjNpv8hX3w6rNQgRTwJyhFtJZoLOTjgbMOFOY2XOPzFxmTR8uVBPJWv44khJANrDQVpOm+41AG+5LMPCbnpP54DWD82S/+W3/AHGD3xSjfkv5EysGk4Wf/9k=)](https://github.com/TeissierYannis)
[![RichMartins](https://img.shields.io/badge/richmartins-visit-blue.svg?style=for-the-badge&logo=data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCAAZABkDASIAAhEBAxEB/8QAGAAAAwEBAAAAAAAAAAAAAAAABAUGBwP/xAA0EAABBAECAgUJCQAAAAAAAAABAgMEEQUSIQAGExUiMUEUFiQ2VXOTstEyN0JWYnSUsdP/xAAXAQEBAQEAAAAAAAAAAAAAAAACAwEE/8QAGhEBAQEBAAMAAAAAAAAAAAAAAQARAhIhUf/aAAwDAQACEQMRAD8AoH+aMtmcFjMFkAlnFQ5SzDa8nAWkKPYJdBVq1aySdwU2oDbZniGHJuXj4TDx2231uBlEh2PqSo9x0CwGkpoC71GiO1seE0ZDrcDlt5hx6Lj1y0JKWHG1W2SOk7NbJ77pRrfYVQ1yXOxLcWFgcSoCdOkqLLkdw9IhhBJedUoG7KWykEbBa0+II43pz0XDyP2kuYcHk8OiKOs2s3BLpcDrTeinW1UQTZKRteqjtX2diOvXk78vs/DT9eNKbmoflOuOk9wDTrzyiCob6LV4HxH6eBtWN9jYj+E9/nwNmbYg1y5NwuIx2UnwldSS31twkBOhC26QEANAlYoCjdnZV6vws2cay16Q2uQQnUUP4+WWJTSXFBRaVSkhxvWNVBQIrs2Ko7nn7q+TfePfNxCcler3LXvB8iOGm0wByrJWNcyboDKczLcTpV0T0qQhgEG0lxtTy1Obpugk2QBYAJJfmxzV7aifCi/XgqJ6t5L9sf7Xwg4NTxC//9k=)](https://github.com/richmartins)
[![Logan-Developer](https://img.shields.io/badge/logandeveloper-visit-blue.svg?style=for-the-badge&logo=data:image/jpg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCAAyADIDASIAAhEBAxEB/8QAGwABAAMBAAMAAAAAAAAAAAAAAAUGBwQCCAn/xAA3EAAABQMCAwMICwEAAAAAAAAAAQIDBAUGEQcSEyFRFzHSNlJUYXGSk7EUFSMyNDVyc3ShsrP/xAAYAQEBAQEBAAAAAAAAAAAAAAAABAUDAv/EACoRAAIBAgIHCQAAAAAAAAAAAAABAgMEIjEFEhMhQVGxERQyQlJxoeHx/9oADAMBAAIRAxEAPwD6A31fSbJbhqVDOZ9JNZYJzZt249R9Rz2PqMi9ZsmOmAqIbLZObjd3554x3EK1r1+Hov6nfkgRuhP53Uv45f6Ibkbak7F1msX2Suctrq8DRr3vBNl01iWqKcsnXeFsJezHIzznB9BEWZqgi8KwcBNOVFMmlOcQ3t3cZcsbS6iQ1DtB+8qVHiR32462nydNThGZGW0yxy9ohLC0xmWjXTnPzGH0Gypva2Ss5My6+wT042vdm5+Pfz/D03U192RarwuZNpUVVQVHOUSVpRwyXt7/AF4MVm1dW27or0amJpio5vbvtDf3Ywk1d20ug6NZfIl399v5jMdJ/L6mex3/AJLFFtbUqlpOrJYl29DxOpJVFFZHsOAAMMrKTqXZE682qemE9HaOOazVx1KLO7bjGCPoKpRYD2jchc6rmiW1MTwUJhGalEZGR5PcSeQ2EUrU60J13QITME2iWy4a1cVRpLBljoY1La5bSt6jwceuZwnDzxzIzt0o/oM73UeIO3Sj+gzvdR4hT+xW4fOh/FPwh2K3D50P4p+EaWw0d6vk4a9bkWKsXbH1UifUFMZdjS3FE6TkvBIwnmf3TM/6HlZGlVVtq5odRkyYbjLO/clpazUeUKSWMpIu8w0/00q9s3KzPmKjGwlC0nw3DM8mWC5YGqCK4uFQToWzwNe+eZ1hBzxTzAAAxikAAAAAAAAAAAAAAAAAAAAAAAAAAAAAP//Z)](https://github.com/Logan-Developer)