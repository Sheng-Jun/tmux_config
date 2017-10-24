# tmux_config

I change the hot-key to be Ctrl+x, instead of Ctrl+b, which has a further seperation on a keyboard.

Moreover, I change parts of keys to be vim-like style.

To activate these settings, put ".tmux.config" at your home directory.

tmux session
============

1. Quickly create a tmux session: 
 
        tmux

In this case, the created sessions will be named by numbers.

To rename a session: Ctrl+x then $

2. Create a named tmux session: 

        tmux new-session -s session-name  [OR]
        tmux new -s session-name

3. Check current sessions:

        tmux list-sessions  [OR]
        tmux ls
        
4. Exit the current session (as the way you logout on the terminal):

        exit

5. Leave the current session but keep your jobs running: Ctrl+x then d (detach)

To resume the session:

        tmux attach-session -t session-name  [OR]
        tmux a -t session-name
        
6. Stop a session:

        tmux kill-session -t session-name
        
7. Stop all sessions:

        tmux kill-server
    

tmux window
============

tmux provides an environment of mulitple workspace/desktops, which are called "windows".

As you create a session, there is a window.

1. Create a new window: Ctrl+x then c

2. Move to next/previous window: Ctrl+x then n/p

3. Close the current window:

       exit


tmux pane
============

As you create a window, there is a pane.

tmux could split the current window to be several panes.

1. Split the window horizontally: Ctrl+x then s

2. Split the window vertically: Ctrl+x then v 

3. Move to other panes: Ctrl+x then Arrow-up/down/right/left or h/j/k/l

4. Adjust the location of boundary among panes: Ctrl+x then hit Ctrl+Arrow-up/down/right/left for several times

5. Enlarge the current pane to fullscreen: Ctrl+x then z

To resume: Ctrl+x then z

6. Scroll up/down a pane: Ctrl+x then PageUp/PageDown

To exit the scrolling mode: Enter

P.S. Mouse wheel can't scroll the pane. Instead of that, it can show the command history.

7. Home and End are also deactivated in tmux panes.

Alternatively, use Ctrl+A and Ctrl+E as Home and End.

8. copy text in tmux:

If it is one-line text, as usual, just select the text and then copy.

If it was not, we can (1) enter the copy mode: Ctrl+x then \[

(2) move the focus to the text, 

(3) hit Space at the begginning location of the text, 

(4) move to select whole text, 

(5) hit Enter to declare the end of the text, 

(6) Ctrl+x then \] to paste somewhere you like.
