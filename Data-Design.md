# Data Design

## File Table:

1. String Path
2. String Filename
3. Bool hasPermisson
4. String (maybe GUID) SongID

## Song Table:

1. String (maybe GUID) SongID
2. String TrackTitle
3. String[] PrimaryArtistsID
4. String[] FeaturedArtistsID
5. String[] Album
6. String Genre
7. String[] Subgenres
8. String ComposerID
9. String[] PublisherID
10. String[] ProducersID
11. String[] AdditionalContributersID
12. Bool isExplicit
13. String[] LyricsLanguage
14. String[] LyricsPublisherID
15. String[] CompositionOwnersID
16. String? CompositionYear
17. String[] MasterRecordingOwnerID
18. String? YearRecored
19. String[] ReleaseLanguages
20. String[] Moods

## Album Table:

1. String (maybe GUID) AlbumID
2. String[] SongsID
3. String[] PrimaryArtistsID
4. String[] FeaturedArtistsID
5. String[] Moods
6. String[] Genres
7. SomeExternalRatingSystemScore Score
8. SomeInternalRatingSystemScore Score

## Artist Table:

1. String (maybe GUID) ArtistID
2. String ArtistName
3. String ArtistDescription
4. SomeExternalRatingSystemScore Score
5. SomeInternalRatingSystemScore Score,
6. String[] SongsID
7. String[] AlbumsID
8. KeyValue[] SocialMediaLinks,

## Playlists Table:

1. String PlaylistID
2. String[] SongsID
3. String[] Moods
4. String PlaylistAuthor
5. SomeExternalRatingSystemScore Score
6. SomeInternalRatingSystemScore Score,

## Pending/External Playlists Table:

1. String PlaylistID
2. String[] SongsID
3. String PlaylistAuthor
4. String[] Moods
5. SomeExternalRatingSystemScore Score

## Image Table:

1. String ID
2. String Image(base64 encoded)

## Additional Images Table:

1. String ID
2. String[] Image(base64 encoded)

## Link Table (MusicBoard, AllMusic, Other API's):

1. String LinkID
2. String SiteName
3. String SiteURL
4. String ExternalID
5. String ExternalURL

## Similar Songs Table (KeyValue):

1. String SongID: String SongID

## Other Entities Table (KeyValue) (ComposerID, PublisherID, ProducersID, AdditionalContributersID)

1. String ID: Any? Data
