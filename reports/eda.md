# Song Popularity Prediction Project –  

## Exploratory data Analysis (UNIVARIATE ANALYSIS):-
**Numerical Columns :-**
From the graph analysis we get to know that:
* **mode** is a binary valued column which can be treated as **categorical column** <br>
* **key** have only values from 0 to 10 and haence can be treated as **categorical column**

**Categorical Columns :-**
Number of categories in artists: 31437<br>
Number of categories in album_name: 46589<br>
Number of categories in popularity: 101<br>
Number of categories in explicit: 2<br>
Number of categories in time_signature: 5<br>
Number of categories in track_genre: 114

## Correlation Analysis :-
### Popularity VS other Feature :
From both Pearson and Spearman correlations, the relationship between popularity and audio features is very weak.
**Observations**
* Highest positive correlations with popularity:
        --Loudness ≈ 0.05
        --Explicit ≈ 0.04
        --Danceability ≈ 0.03
        --Time signature ≈ 0.03

* Negative correlations with popularity:
        --Instrumentalness ≈ -0.095 (largest negative)
        --Speechiness ≈ -0.045
        --Valence ≈ -0.04
        --Acousticness ≈ -0.025

**Interpretation**
* Instrumental tracks tend to be slightly less popular.
* Songs with vocals tend to gain more popularity than instrumental tracks.
* Explicit songs show slightly higher popularity, but the effect is small.
* No single audio feature strongly determines popularity.


### Strong Relationships Between Audio Features:- 
Some features show strong correlations with each other.

* Energy vs Loudness - Strong positive correlation
* Energy vs Acousticness - trong negative correlation 
* Danceability vs Valence - Moderate positive correlation
* Loudness vs Acousticness - Negative correlation

**Weak Features**
Some features have almost no impact on other variables.
* Key
* Mode
* Tempo
* Time signature

**Interpretation:**
Musical structure characteristics do not strongly influence popularity.

## Relation of features over various popularity buckets
1. Danceability
**Observation:**
* High popularity songs tend to cluster around higher danceability values (≈0.6–0.8).
* Low popularity songs show a slightly wider spread toward lower values.
**Interpretation:**
* More danceable songs tend to have higher popularity.
* Danceability is one of the mild indicators of song success.

2. Energy
**Observation:**
* High popularity songs are concentrated around moderate to high energy levels (0.6–0.9).
* Low popularity songs include more low-energy tracks.
**Interpretation:**
* Energetic songs are slightly more likely to be popular.

3. Loudness
**Observation:**
* High popularity songs tend to cluster around higher loudness values.
* Low popularity songs show slightly lower loudness levels.
**Interpretation:**
* Louder songs tend to be slightly more popular, likely due to higher perceived energy.

4. Mode (Major / Minor)
**Observation:**
* Most songs are in major mode (value 1) across all popularity classes.
**Interpretation:**
* Musical mode has minimal impact on popularity.

5. Acousticness
**Observation:**
* High popularity songs tend to have lower acousticness values.
* Low popularity songs include more highly acoustic tracks.
**Interpretation:**
* Less acoustic (more produced/electronic) songs tend to be more popular.

6. Instrumentalness
**Observation:**
* Most songs have very low instrumentalness.
* High popularity songs show very small instrumental presence.
**Interpretation:**
* Songs with vocals tend to be more popular than instrumental tracks.

7. Valence (Musical Positivity)
**Observation:**
* High popularity songs are slightly concentrated around medium valence values (0.4–0.7).
**Interpretation:**
* Moderately positive songs tend to be more popular, but the relationship is weak.



## Overall Insight
Main findings from the analysis:
* Audio features alone cannot strongly predict popularity.
* Energy and loudness are strongly related.
* Energetic and Danceable Songs Tend to Perform Slightly Better whereas Acoustic songs tend to have lower energy and loudness.
* Genre Plays a More Important Role Than Audio Features
* Musical attributes like key, mode, tempo, and time signature have little influence on popularity.
* Popularity Is Influenced by External Factors


The exploratory data analysis reveals that while certain audio characteristics such as danceability, energy, and loudness show slight associations with popularity, most musical features have weak correlations with song popularity. Genre plays a more significant role, with mainstream genres dominating the high popularity class. This suggests that external factors such as artist reputation, marketing exposure, and audience reach may have a greater impact on determining song success than intrinsic audio attributes alone.