# College Knowledge Database

This is my obsidian vault containing all my college course.
This vault utilize the usage of graph view for better reviewing during exams.

This obsidian vault utilize the usage of [Obsidian_to_anki](https://github.com/ObsidianToAnki/Obsidian_to_Anki) using the regex: 
`((?:[^\n][\n]?)+) #! ?\n*((?:\n(?:^.{1,3}$|^.{4}(?<!<!--).*))+)`

This allows to create a basic Anki card with this patern:

Front of the card #!  
Back of the card

This vault syncing is done via `git` using the [Obsidian Git](https://github.com/denolehov/obsidian-git) plugin. This plugin is also compatible on mobile, allowing this vault to be updated on all my devices.