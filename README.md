# A Data Project: Movie Rate Differences in Two Websites

## Idea

The data is based on The 21st Century’s 100 greatest films polled by BBC.

The final 100 movie list can be found everywhere. But the original webpage which contains the information of the critics and their top 10 choices doesn't exist anymore. Luckily, my professor preserved it [here](http://floatingmedia.com/columbia/BBC.html).

My idea was to examine the rate in different countries of those movies picked by critics. So I chose [IMDb](https://www.imdb.com/), a popular rating website in U.S., and [Douban](https://www.douban.com/), a similar website in China, and scrape the number of people who watched and rated those movies, as well as their rates.

I also tried to scrape the geographic information of the movies. It's hard to decide a movie's birthplace. They can be shot in many places, invested by many companies and acted by actors all around the world. After careful considerations, I finally decided to use the director's birthplace for each movie.

I hope to see the different tastes of eastern and western audiences, as well as of critics and ordinary people.

## Analysis

All of my analysis is done by Python in Jupyter Notebook. I put them [here](https://github.com/AngelineJCQ/bbc-movie-rate-crosscountry/docs/code)

The logic here is:

1. Scrape all BBC list
2. Scrape IMDb info, including:
- the director's name
- the director's birthplace
- the rate
- the number of people who rated the movie
3. Scrape Douban info, including:
- the rate
- the number of people who rated the movie
4. Get the geocode of all the birthplaces
5. Get the final dataframe 
6. Trasfer the dataframe to Json file

## Result

An interactive map.

Each circle is a director's birthplace. The bigger the circle is, the more vote it got from 177 critics selected by BBC in 2016.

Different color means:
![image]()

(It will be proved in the future. I promise. Use bivariate color schemes as my professor suggested)

The map indicates that:

1. Overall, Douban rate is higher than IMDb
2. The movies got more people and higher rate in China cluster in Asia
3. The movies got more people and higher rate in America cluster in America and Europe
4. The movies voted by many critics (larger circles) are usually watched more by American people but rated higher in Chinese website (yellow color)
5. Most directors in the list are from North America and Europe, with few from South America, Africa and Australia
