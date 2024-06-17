# IMDB Datasets

## Dataset Source
Original Source: [IMDB Dataset on Kaggle](https://www.kaggle.com/datasets/ashirwadsangwan/imdb-dataset)

## Loaded Data
The dataset has been loaded into an S3 bucket with the following files:
- `s3://cis9760-lecture9-movieanalysis/name.basics.tsv` (actors)
- `s3://cis9760-lecture9-movieanalysis/title.basics.tsv` (genres)
- `s3://cis9760-lecture9-movieanalysis/title.principals.tsv` (movie actors)
- `s3://cis9760-lecture9-movieanalysis/title.ratings.tsv` (movie ratings)

## Data Description
### `name.basics.tsv.gz`
- `nconst` (string): Alphanumeric unique identifier of the name/person.
- `primaryName` (string): Name by which the person is most often credited.
- `birthYear` (YYYY): Year of birth in YYYY format.
- `deathYear` (YYYY): Year of death in YYYY format if applicable, else empty.
- `primaryProfession` (array of strings): Top 3 professions of the person.
- `knownForTitles` (array of tconsts): Titles the person is known for.

### `title.basics.tsv.gz`
- `tconst` (string): Alphanumeric unique identifier of the title.
- `titleType` (string): Type/format of the title (e.g., movie, short, tvseries).
- `primaryTitle` (string): Popular title used by filmmakers on promotional materials.
- `originalTitle` (string): Original title in the original language.
- `isAdult` (boolean): 0 for non-adult title, 1 for adult title.
- `startYear` (YYYY): Release year of a title or series start year for TV series.
- `endYear` (YYYY): End year of TV series, empty for other title types.
- `runtimeMinutes` (int): Primary runtime of the title in minutes.
- `genres` (string array): Up to three genres associated with the title.

### `title.principals.tsv`
- `tconst` (string): Alphanumeric unique identifier of the title.
- `ordering` (int): Number to uniquely identify rows for a given titleId.
- `nconst` (string): Alphanumeric unique identifier of the name/person.
- `category` (string): Category of job that person was in.
- `job` (string): Specific job title if applicable, else empty.
- `characters` (string): Name of the character played if applicable, else empty.

### `title.ratings.tsv.gz`
- `tconst` (string): Alphanumeric unique identifier of the title.
- `averageRating` (float): Weighted average of all the individual user ratings.
- `numVotes` (int): Number of votes the title has received.

## Cluster and Notebook Configuration
![Cluster Configuration](<img width="481" alt="image" src="https://github.com/linalan1231/IMDB/assets/70352593/acf30f48-4e5b-458d-9283-2d4df4bbafb1">)
![Notebook Configuration](<img width="357" alt="image" src="https://github.com/linalan1231/IMDB/assets/70352593/b017ebfe-9193-4e0d-87fb-5c7d42d19a3d">)
