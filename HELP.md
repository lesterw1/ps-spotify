# Documentation for ps-spotify
This is the combined documentation for the ps-spotify cmdlets.
<br/>Last updated on Sunday 11/22/2020 10:24 UTC
<br/><br/>

| Cmdlet | Synopsis |
| --- | --- |
| [Find-SpotifyItem](#find-spotifyitem) | Returns Spotify catalog information about artists, albums, tracks or playlists that match a keyword string. |
| [Get-SpotifyAccessToken](#get-spotifyaccesstoken) | Always returns a usable Spotify access token to use. This cmdlet checks if your current access token is still valid and if that's not the case, it will refresh it for you. |
| [Get-SpotifyAlbum](#get-spotifyalbum) | Returns Spotify catalog information for a single album. |
| [Get-SpotifyAlbums](#get-spotifyalbums) | Returns Spotify catalog information for multiple albums. |
| [Get-SpotifyCategories](#get-spotifycategories) | Returns a list of categories used to tag items in Spotify. |
| [Get-SpotifyCategory](#get-spotifycategory) | Returns a single category used to tag items in Spotify. |
| [Get-SpotifyConnectDevice](#get-spotifyconnectdevice) | Returns the currently active Spotify Connect device. |
| [Get-SpotifyConnectDevices](#get-spotifyconnectdevices) | Returns a list of Spotify Connect devices listed on the connected Spotify account. |
| [Get-SpotifyCurrentlyPlaying](#get-spotifycurrentlyplaying) | Returns the currently playing track. |
| [Get-SpotifyFeaturedPlaylists](#get-spotifyfeaturedplaylists) | Returns a list of featured playlists. |
| [Get-SpotifyNewReleases](#get-spotifynewreleases) | Returns a list of newly released albums on Spotify. |
| [Get-SpotifyTrack](#get-spotifytrack) | Returns Spotify catalog information for a single track identified by its unique Spotify ID. |
| [Get-SpotifyTracks](#get-spotifytracks) | Returns Spotify catalog information for multiple tracks. |
| [Get-SpotifyUser](#get-spotifyuser) | Returns Spotify catalog information for a single track identified by its unique Spotify ID. |
| [Invoke-SpotifyConnectPrevious](#invoke-spotifyconnectprevious) | Sets the current song to the previous song using Spotify Connect. |
| [Invoke-SpotifyConnectSkip](#invoke-spotifyconnectskip) | Skips the current song using Spotify Connect. |
| [Set-SpotifyConnectPause](#set-spotifyconnectpause) | Pause Spotify playback using Spotify Connect. |
| [Set-SpotifyConnectPlay](#set-spotifyconnectplay) | Start Spotify playback using Spotify Connect. |
| [Set-SpotifyConnectPlayer](#set-spotifyconnectplayer) | Transfer playback to one or more Spotify Connect devices. |
| [Set-SpotifyConnectRepeat](#set-spotifyconnectrepeat) | Set-SpotifyConnectRepeat [-State] <string> [[-DeviceID] <string>] [<CommonParameters>] |
| [Set-SpotifyConnectSeek](#set-spotifyconnectseek) | Seeks to the given position in the userâ€™s currently playing track. |
| [Set-SpotifyConnectVolume](#set-spotifyconnectvolume) | Set-SpotifyConnectVolume [-VolumePercent] <int> [[-DeviceID] <string>] [<CommonParameters>] |

---

## Find-SpotifyItem

### Synopsis

Returns Spotify catalog information about artists, albums, tracks or playlists that match a keyword string.

### Syntax

Find-SpotifyItem [-Type] <Array> [-Query] <String> [<CommonParameters>]

### Description



### Parameters

	-Type <Array>
	    Required. A comma-separated list of item types to search across. Valid types are: album, artist, playlist, and track.

	-Query <String>

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Find-SpotifyItem -Type track -Query "suburban train"



---
## Get-SpotifyAccessToken

### Synopsis

Always returns a usable Spotify access token to use. This cmdlet checks if your current access token is still valid and if that's not the case, it will refresh it for you.

### Syntax

Get-SpotifyAccessToken [<CommonParameters>]

### Description



### Parameters

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyAccessToken



---
## Get-SpotifyAlbum

### Synopsis

Returns Spotify catalog information for a single album.

### Syntax

Get-SpotifyAlbum [-Album] <String> [<CommonParameters>]

### Description



### Parameters

	-Album <String>
	    Required. The Spotify ID for the album.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyAlbum 0sNOF9WDwhWunNAHPD3Baj



---
## Get-SpotifyAlbums

### Synopsis

Returns Spotify catalog information for multiple albums.

### Syntax

Get-SpotifyAlbums [-Albums] <Array> [<CommonParameters>]

### Description



### Parameters

	-Albums <Array>
	    Required. The Spotify IDs for the albums, supplied as an array.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyAlbums "41MnTivkwTO3UUJ8DrqEJJ","6JWc4iAiJ9FjyK0B59ABb4"



---
## Get-SpotifyCategories

### Synopsis

Returns a list of categories used to tag items in Spotify.

### Syntax

Get-SpotifyCategories [[-Locale] <String>] [[-Country] <String>] [[-Limit] <String>] [[-Offset] <String>] [<CommonParameters>]

### Description



### Parameters

	-Locale <String>
	    Optional. The desired language, consisting of a lowercase ISO 639 language code and an uppercase ISO 3166-1 alpha-2 country code, joined by an underscore.

	-Country <String>
	    Optional. A country: an ISO 3166-1 alpha-2 country code. Provide this parameter if you want the list of returned items to be relevant to a particular country.

	-Limit <String>
	    Optional. The maximum number of items to return. Default: 20. Minimum: 1. Maximum: 50.

	-Offset <String>
	    Optional. The index of the first item to return. Default: 0 (the first object). Use with limit to get the next set of items.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyCategories



---
## Get-SpotifyCategory

### Synopsis

Returns a single category used to tag items in Spotify.

### Syntax

Get-SpotifyCategory [-CategoryID] <String> [[-Locale] <String>] [[-Country] <String>] [<CommonParameters>]

### Description



### Parameters

	-CategoryID <String>
	    Required. The Spotify category ID for the category.

	-Locale <String>
	    Optional. The desired language, consisting of a lowercase ISO 639 language code and an uppercase ISO 3166-1 alpha-2 country code, joined by an underscore.

	-Country <String>
	    Optional. A country: an ISO 3166-1 alpha-2 country code. Provide this parameter if you want the list of returned items to be relevant to a particular country.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyCategory



---
## Get-SpotifyConnectDevice

### Synopsis

Returns the currently active Spotify Connect device.

### Syntax

Get-SpotifyConnectDevice [<CommonParameters>]

### Description



### Parameters

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyConnectDevice



---
## Get-SpotifyConnectDevices

### Synopsis

Returns a list of Spotify Connect devices listed on the connected Spotify account.

### Syntax

Get-SpotifyConnectDevices [<CommonParameters>]

### Description



### Parameters

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyConnectDevices



---
## Get-SpotifyCurrentlyPlaying

### Synopsis

Returns the currently playing track.

### Syntax

Get-SpotifyCurrentlyPlaying [<CommonParameters>]

### Description



### Parameters

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyCurrentlyPlaying



---
## Get-SpotifyFeaturedPlaylists

### Synopsis

Returns a list of featured playlists.

### Syntax

Get-SpotifyFeaturedPlaylists [[-Locale] <String>] [[-Country] <String>] [[-Limit] <String>] [[-Offset] <String>] [<CommonParameters>]

### Description



### Parameters

	-Locale <String>
	    Optional. The desired language, consisting of a lowercase ISO 639 language code and an uppercase ISO 3166-1 alpha-2 country code, joined by an underscore.

	-Country <String>
	    Optional. A country: an ISO 3166-1 alpha-2 country code. Provide this parameter if you want the list of returned items to be relevant to a particular country.

	-Limit <String>
	    Optional. The maximum number of items to return. Default: 20. Minimum: 1. Maximum: 50.

	-Offset <String>
	    Optional. The index of the first item to return. Default: 0 (the first object). Use with limit to get the next set of items.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyFeaturedPlaylists



---
## Get-SpotifyNewReleases

### Synopsis

Returns a list of newly released albums on Spotify.

### Syntax

Get-SpotifyNewReleases [[-Country] <String>] [[-Limit] <String>] [[-Offset] <String>] [<CommonParameters>]

### Description



### Parameters

	-Country <String>
	    Optional. A country: an ISO 3166-1 alpha-2 country code. Provide this parameter if you want the list of returned items to be relevant to a particular country.

	-Limit <String>
	    Optional. The maximum number of items to return. Default: 20. Minimum: 1. Maximum: 50.

	-Offset <String>
	    Optional. The index of the first item to return. Default: 0 (the first object). Use with limit to get the next set of items.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyNewReleases



---
## Get-SpotifyTrack

### Synopsis

Returns Spotify catalog information for a single track identified by its unique Spotify ID.

### Syntax

Get-SpotifyTrack [-Track] <String> [<CommonParameters>]

### Description



### Parameters

	-Track <String>
	    Required. The Spotify ID for the track.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyTrack 3n3Ppam7vgaVa1iaRUc9Lp



---
## Get-SpotifyTracks

### Synopsis

Returns Spotify catalog information for multiple tracks.

### Syntax

Get-SpotifyTracks [-Tracks] <Array> [<CommonParameters>]

### Description



### Parameters

	-Tracks <Array>
	    Required. The Spotify IDs for the tracks, supplied as an array.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyTracks "41MnTivkwTO3UUJ8DrqEJJ","6JWc4iAiJ9FjyK0B59ABb4"



---
## Get-SpotifyUser

### Synopsis

Returns Spotify catalog information for a single track identified by its unique Spotify ID.

### Syntax

Get-SpotifyUser [-User] <String> [<CommonParameters>]

### Description



### Parameters

	-User <String>
	    Required. The Spotify ID for the user.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Get-SpotifyUser tuggareutangranser



---
## Invoke-SpotifyConnectPrevious

### Synopsis

Sets the current song to the previous song using Spotify Connect.

### Syntax

Invoke-SpotifyConnectPrevious [[-DeviceID] <String>] [<CommonParameters>]

### Description



### Parameters

	-DeviceID <String>
	    Optional. The id of the device this command is targeting. If not supplied, the user's currently active device is the target.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS C:\>Go back to the previous song

PS /Users/bart> Invoke-SpotifyConnectPrevious



---
## Invoke-SpotifyConnectSkip

### Synopsis

Skips the current song using Spotify Connect.

### Syntax

Invoke-SpotifyConnectSkip [[-DeviceID] <String>] [<CommonParameters>]

### Description



### Parameters

	-DeviceID <String>
	    Optional. The id of the device this command is targeting. If not supplied, the user's currently active device is the target.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS C:\>Skip the current song

PS /Users/bart> Invoke-SpotifyConnectSkip



---
## Set-SpotifyConnectPause

### Synopsis

Pause Spotify playback using Spotify Connect.

### Syntax

Set-SpotifyConnectPause [[-DeviceID] <String>] [<CommonParameters>]

### Description



### Parameters

	-DeviceID <String>
	    Optional. The id of the device this command is targeting. If not supplied, the user's currently active device is the target.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS C:\>Pause playback

PS /Users/bart> Set-SpotifyConnectPause



---
## Set-SpotifyConnectPlay

### Synopsis

Start Spotify playback using Spotify Connect.

### Syntax

Set-SpotifyConnectPlay [[-ContextURI] <String>] [[-URIs] <Array>] [[-Offset] <Int32>] [[-Play] <Boolean>] [<CommonParameters>]

### Description



### Parameters

	-ContextURI <String>
	    Optional. Spotify URI of the context to play. Valid contexts are albums, artists & playlists.

	-URIs <Array>
	    Optional. Spotify track URIs to play.

	-Offset <Int32>
	    Optional. Indicates from where in the context playback should start. Only available when ContextURI corresponds to an album or playlist object, or when the URIs parameter is used. Offset starts at 0 and can't be negative.

	-Play <Boolean>

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS C:\>Play an album.

PS /Users/bart> Set-SpotifyConnectPlay -ContextURI "spotify:album:1Je1IMUlBXcx1Fz0WE7oPT"




-------------------------- EXAMPLE 2 --------------------------

PS C:\>Play two songs, start at offset 0

PS /Users/bart> Set-SpotifyConnectPlay -URIs "spotify:track:6KeXJbrg02axATKVgdW8am","spotify:track:0Dkibk70FDp6t7eOZNemNQ" -Offset 0




-------------------------- EXAMPLE 3 --------------------------

PS C:\>Start playing with the currently available queue

PS /Users/bart> Set-SpotifyConnectPlay



---
## Set-SpotifyConnectPlayer

### Synopsis

Transfer playback to one or more Spotify Connect devices.

### Syntax

Set-SpotifyConnectPlayer [-Devices] <Array> [[-Play] <Boolean>] [<CommonParameters>]

### Description



### Parameters

	-Devices <Array>
	    The device or multiple devices to connect to.

	-Play <Boolean>
	    Enable playback status on devices, or just se.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS /Users/bart>Set-SpotifyConnectPlayer -Devices "10012","10013","10014" -Play $false



---
## Set-SpotifyConnectRepeat

### Synopsis

Set-SpotifyConnectRepeat [-State] <string> [[-DeviceID] <string>] [<CommonParameters>]

### Syntax

syntaxItem                                                                                                          
----------                                                                                                          
{@{name=Set-SpotifyConnectRepeat; CommonParameters=True; WorkflowCommonParameters=False; parameter=System.Object[]}}

### Description



### Parameters

	-DeviceID <string>

	-State <string>



---
## Set-SpotifyConnectSeek

### Synopsis

Seeks to the given position in the userâ€™s currently playing track.

### Syntax

Set-SpotifyConnectSeek [-PositionMS] <Int32> [[-DeviceID] <String>] [<CommonParameters>]

### Description



### Parameters

	-PositionMS <Int32>
	    Required. The position in milliseconds to seek to. Must be a positive number. Passing in a position that is greater than the length of the track will cause the player to start playing the next song.

	-DeviceID <String>
	    Optional. The id of the device this command is targeting. If not supplied, the user's currently active device is the target.

### Examples

-------------------------- EXAMPLE 1 --------------------------

PS C:\>Seek to the 10th second of the current playing track

PS /Users/bart> Set-SpotifyConnectSeek -PositionMS 10000



---
## Set-SpotifyConnectVolume

### Synopsis

Set-SpotifyConnectVolume [-VolumePercent] <int> [[-DeviceID] <string>] [<CommonParameters>]

### Syntax

syntaxItem                                                                                                          
----------                                                                                                          
{@{name=Set-SpotifyConnectVolume; CommonParameters=True; WorkflowCommonParameters=False; parameter=System.Object[]}}

### Description



### Parameters

	-DeviceID <string>

	-VolumePercent <int>



---

*This combined documentation page was created using https://github.com/lesterw1/AzureExtensions/tree/master/Ax.Markdown cmdlet.*

