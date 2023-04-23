# Data Description

The dataset (Spotify Tracks DB) was made available thanks to by Zaheen Hamidani and retrieved from Kaggle: [https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db](https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db)
 
`Lyrics` was added into the dataset though webscrapping.  

### What is inside the dataset?
The dataset contains details from 232,725 song tracks across 26 music genre. Each track consists of 18 unique data variables.  

---
### Description of each data variable
Descriptions of each data variable are found from Spotify Web Api for developers: [https://developer.spotify.com/documentation/web-api](https://developer.spotify.com/documentation/web-api)

**`genre`**
**Data type:** Categorical and Ordinal
The genre of the song tack based on its album. There are 26 different genres in this dataset found when we explored the data is as of below:
 
Comedy, Soundtrack, Indie, Jaz, Pop, Electronic, Children’s Music, Folk, Hip-Hop, Rock, Alternative, Classical, Rap, World, Soul, Blues, R&B, Anime, Reggaeton, Ska, Reggae, Dance, Country, Opera, Movie, A Capella, 

**`artist_name`**
**Data type:** Categorical and Nominal
The name of the artist of the particular song track

**`track_name`**
**Data type:** Categorical and Nominal
The name of the song track

**`track_id`** 
**Data type:** Categorical and Nominal
The spotify ID of the track. It is the base-62 identifier found at the end of the Spotify URI (see above) for an artist, track, album, playlist, etc. Unlike a Spotify URI, a Spotify ID does not clearly identify the type of resource; that information is provided elsewhere in the call.

**`popularity`**
**Data type:** Categorical and Ordinal (integer form)
The popularity of the track. The value will be between `0 and 100`, with `100` being the most popular. The popularity is calculated by algorithm and is based, in the most part, on the total number of plays the track has had and how recent those plays are.

Generally speaking, songs that are being played a lot now will have a higher popularity than songs that were played a lot in the past. Duplicate tracks (e.g. the same track from a single and an album) are rated independently. Artist and album popularity is derived mathematically from track popularity.

***Note**: the popularity value may lag actual popularity by a few days: the value is not updated in real time.*

**`acousticness`**
**Data type:** Numerical
A confidence measure from `0.0 to 1.0` of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.
Example value: `0.00242`Range: `0` - `1`

**`danceability`**
**Data type:** Numerical
Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. `A value of 0.0 is least danceable and 1.0 is most danceable.`
Example value: `0.585`

**`duration_ms`**
**Data type:** Numerical
The duration of the track in milliseconds.
Example value: `237040`

**`energy`**
**Data type:** Numerical
Energy is a measure from `0.0 to 1.0` and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.
Example value: `0.842`

**`instrumentalness`**
Data type: Numerical
Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.
Example value: `0.00686`

**`key`**
Data type: Categorical and Ordinal
The key the track is in. Integers map to pitches using standard [Pitch Class notation](https://en.wikipedia.org/wiki/Pitch_class). E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.

**`liveness`**
Data type: Numerical
Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.
Example value: `0.0866`

**`loudness`**
Data type: Numerical
The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db.
Example value: `-5.883`

**`mode`**
**Data type:** Categorical and Nominal
Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived.
**2 categories:**
Major
Minor

**`speechiness`**
Data type: Numerical
Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.
Example value: `0.0556`

**`tempo`**
Data type: Numerical
The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.
Example value: `118.211`

**`time_signature`**
Data type: Categorical
An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".
Example value: `4`Range: `3` - `7`

**`valence`**
Data type: Numerical
A measure from `0.0 to 1.0` describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).
Example value: `0.428`Range: `0` - `1`

Variables that we have added (not found on Spotify's API)
`lyrics` of the song
`modal_key` of the song which tells you which major or minor key the song is in on average. 

Compiled by: Elaine and Ye Chuan