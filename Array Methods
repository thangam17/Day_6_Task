// Get all the countries from the Asia continent /region using the Filter function

var xhr = new XMLHttpRequest;
xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();
xhr.onload = function()
{
    var responseObj = xhr.response;

    var cont = responseObj.filter(function(item)
    {
        return item.continents == 'Asia';
    })

    var country = cont.map(function(item1)
    {
        return item1.name.common;
    })

    console.log(country);
    
}

// Get all the countries with a population of less than 2 lakhs using Filter function

var xhr = new XMLHttpRequest;
xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();
xhr.onload = function()
{

var responseObj = xhr.response;
var country = responseObj.filter(function(item)
{
    return item.population < 200000


})
console.log(country)

var name1 = country.map(function(show)
{
    return show.name.common

})
console.log(name1)
}

//Print the total population of countries using reduce function

var xhr = new XMLHttpRequest;
xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json';
xhr.send();

xhr.onload = function()
{
    var responseObj = xhr.response;
    var res = responseObj.map(function(item)
    {
        return item.population

    })
    var tpop = res.reduce(function(item1,item2)
    {

        return item1 + item2;

    })

    console.log(tpop)
};

//Print the country which uses US Dollars as currency.

var usd = new XMLHttpRequest();
usd.open("GET", "https://restcountries.com/v3.1/all");
usd.send();
usd.onload = () => {
    let data = JSON.parse(usd.response);
     
    let ans = data.filter((item) => (item.currencies !== undefined))
    
    let realanswer = ans.filter((data) =>  {
    for (let key in data.currencies) {
        if(data.currencies[key].name === "United States dollar"){
            return data;
      }
    }
    })
   
      console.log(realanswer); 
}


// Print the following details name, capital, flag using forEach function

var xhr = new XMLHttpRequest;
xhr.open('GET', 'https://restcountries.com/v3.1/all');
xhr.responseType = 'json'
xhr.send();

xhr.onload = function()
{
    var responseObj = xhr.response;

    responseObj.forEach (function(element)
    {

        console.log(element.flag)

    })
    responseObj.forEach (function(element)
    {

        console.log(element.name)

    })
    responseObj.forEach (function(element)
    {

        console.log(element.capital)

    })
}
