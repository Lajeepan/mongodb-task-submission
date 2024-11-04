## Create a Database called movies.
` use movies `

## Create a collection called moviedetails.
`db.createCollection("moviedetails")`

## Create above 5 movie documents into a moviedetails collection.
```sh
 db.moviedetails.insertMany([
    { title: "Movie A", director: "Lokesh Kanakaraj", year: 2023, genre: "Action" },
    { title: "Movie B", director: "Lokesh Kanakaraj", year: 2022, genre: "Thriller" },
    { title: "Movie C", director: "Magizh Thirumeni", year: 2025, genre: "Drama" },
    { title: "Movie D", director: "Director 4", year: 2021, genre: "Comedy" },
    { title: "Movie E", director: "Director 5", year: 2024, genre: "Horror" }
]) ```


## List all documents created
` db.moviedetails.find() `


## List Lokesh Kanakaraj’s movies.
` db.moviedetails.find({ director: "Lokesh Kanakaraj" }) `



## List Lokesh Kanakaraj’s movies released in 2023. 
` db.moviedetails.find({ director: "Lokesh Kanakaraj", year: 2023 }) `



## Delete the movie which you don’t like. 
` db.moviedetails.deleteOne({ title: "Movie D" }) `


## Add the movie which is your favourite.
` db.moviedetails.insertOne({ title: "Favorite Movie", director: "Favorite Director", year: 2020, genre: "Drama" })`


## List movie Directed by Magizh Thirumeni in 2025.
` db.moviedetails.find({ director: "Magizh Thirumeni", year: 2025 }) `


## List out the Director’s Name in your document.
` db.moviedetails.distinct("director") `