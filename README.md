package com.company;

public class Main {

    public static void main(String[] args) {

        Movie movie1=new Movie("Haikyui", "PG", "2019");
        Movie movie2=new Movie("Food Wars", "PG", "2020");

        movie1.setAnime("Aldnoah zero");
        movie2.setYear("2014");
        movie2.setRating("PG-18");

        System.out.println(movie1.getAnime());
        System.out.println(movie2.getYear());
        System.out.println(movie2.getRating());

    }
}

package com.company;

public class Movie {

    private String anime;
    private String rating;
    private String year;

    public Movie(String anime, String rating, String year){
        this.anime=anime;
        this.rating=rating;
        this.year=year;
    }
    public String getAnime() {
        return anime;
    }

    public void setAnime(String anime) {
        this.anime = anime;
    }

    public String getRating(){
        return rating;
    }

    public void setRating(String rating){
        if(rating.equals("PG") || rating.equals("PG-13") || rating.equals("R")) {
            this.rating = rating;
        }else{
            this.rating="NR";
        }
    }

    public String getYear(){
        return year;
    }

    public void setYear(String year){
        if(year.equals(2018) || this.year.equals(2019) || this.year.equals(2020) ) {
            this.year = year;
        }else{
            this.year="Invalid";
        }
    }




}
