Introduction:

	
  This documentation provides a clear and concise explanation of the Lyrics Fetcher application. The application is built using Python and the tkinter library for the graphical user interface (GUI). It integrates with the Genius API, using the lyricsgenius library, to fetch and display song lyrics based on the artist and song name provided by the user.



Prerequisites:

  1)Python 3.12.2
	
  2)Required libraries: tkinter and lyricsgenius.



1)lyricsgenius:
	 
    A library to interact with the Genius API to fetch lyrics for the given song.

2)tkinter:
 
    A standard GUI library in Python which is used to create gui interface for our code.

3)messagebox: 
 
  it is a module in tkinter to show message boxes.



genius:
	
  It is used to Initializes the Genius API client with my access token.
	and i used that access token in my program to connect with genius server.


artist = artist_entry.get(): It Retrieves the artist name from the input field.

song = song_entry.get(): it is used to Retrieves the song name from the input field filled by end user.

genius.search_song(song, artist): Searches for the song lyrics using the Genius API.

lyrics_text.delete("1.0", tk.END): Clears the previous details of the lyrics entered by end user.

lyrics_text.insert(tk.END, song_data.lyrics): To Inserts the fetched lyrics into the text area.

messagebox.showerror:  It Displays an error message if the song is not found or if any error occurs.

messagebox.showwarning: If any one of field i.e artist name or song name not entered then it Displays a warning message.



root = tk.Tk(): it Initializes the main window.

root.title("Lyrics Fetcher"): Sets the title of the window to Lyrics Fetcher

root.geometry("600x400"): Sets the dimensions of the window to 600*400




tk.Label: this function will Creates labels for the artist and song input fields.

tk.Entry: Creates input fields for the artist and song names.

pack(pady=5): Adds padding around the widgets for better spacing.



tk.Button: Creates a button that calls the fetch_lyrics function when clicked.

command=fetch_lyrics: Binds the button click event to the fetch_lyrics function.

pack(pady=10): Adds padding around the button.



tk.Text: it Creates a text area to display the fetched lyrics.

wrap='word': Wraps text at word boundaries.

height=15, width=60: Sets the dimensions of the text area.

pack(pady=10): Adds padding around the text area.



root.mainloop(): 

  this function Starts the main event loop, which waits for user interaction and updates the GUI accordingly.



Run the script:


  This will open a window where you can enter the artist and song name to fetch and display the lyrics.



Conclusion

 This application allows users to fetch song lyrics by entering the artist's name and the song title. The tkinter library is used to create a user-friendly GUI, and the lyricsgenius library interacts with the Genius API to retrieve the lyrics.
