Currency converter

Front end deploy URL : https://shimmering-brioche-60331f.netlify.app/

Fetch API from Frankfurter API:

Documentation  :
  
    The Frankfurter API tracks foreign exchange references rates published by the European Central Bank. The data refreshes around 16:00 CET every working day.

    Frankfurter integrates seamlessly with libraries like Money.js and Dinero.js.

Usage
    
    The API is organised around paths that designate the requested date or date range.

Conversion

    You can convert any value between currencies using the above endpoints in combination with the amount parameter.

    Below, we convert 10 British Pounds to US Dollars.

            const host = 'api.frankfurter.app';
            fetch(`https://${host}/latest?amount=10&from=GBP&to=USD`)
            .then(resp => resp.json())
            .then((data) => {
            alert(`10 GBP = ${data.rates.USD} USD`);
            });

    A better approach is to fetch rates once and convert client-side using Money.js or Dinero.js.


