# Book My Show LLD

## Requirements
1. List Cities where cinemas are located.
2. Each Cinema can have multiple Audis and each Audi can only run one show at a time.
3. Each movie have multiple shows.
4. Customers should be able to search movies based on title, genre, language and city name.
5. Once user selects the movie, application should display cinemas list with available shows.
6. When a user book the show, he/she should have the option to choose seats.
7. After selecting seats, user should be able to book tickets and do payment.

## First Attempt Solution

<details>
  
<summary> Database Models </summary>
  
<summary> Cities </summary>

```
  class Cities {
    private string name;
    Cities(string name) {
      this.name = name;
    }
  }
```

<summary> Cinemas </summary>

```
  class Cinemas {
    private string name;
    private int city_id;
    Cities(string name, int city_id) {
      this.name = name;
      this.city_id = city_id;
    }
  }
```

<summary> Audis </summary>

```
  class Audis {
    private string name;
    private int cinema_id;
    Audis(string name, int cinema_id) {
      this.name = name;
      this.cinema_id = cinema_id;
    }
  }
```


<summary> Movies </summary>

```
  class Movies {
    private string name;
    private string genre;
    private string languages;
    private date release_date;
    Movies(string name, string genre, string languages, Date release_date) {
      this.name = name;
      this.genre  = genre;
      this.languages = languages;
      this.release_date = release_date;
    }
  }
```

<summary> Shows </summary>

```
  class Shows {
    private int audi_id;
    private int movie_id;
    Shows(int audi_id, int movie_id) {
      this.audi_id = audi_id;
      this.movie_id  = movie_id;
    }
  }
```

<summary> Seats </summary>

```
  class Shows {
    private int seat_number;
    private bool is_filled;
    Shows(int seat_number, bool is_filled) {
      this.seat_number = seat_number;
      this.is_filled  = is_filled;
    }
  }
```

</details>
