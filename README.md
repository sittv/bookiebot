# BookieBot
*The bot that will come after you if you don't return what you borrow*

BookieBot is a project to create an API and Slackbot to maintain the SITTV inventory.

## Uses
- "Keep the books" i.e. keep track of who has borrowed what and when it's due
- Notification system to alert users when they never signed their equipment back in
- Answer queries about what is due when
- Maintain a registry of producers

## Commands
List of commands for communicating with the BookieBot

### current checkouts
List of all 

Modifiers: __group__

### help
Displays the following help message
```
current checkouts
help
info [<item>...]
status
update producers <new_producer> <production>
what does <user> owe?
what is due by <date>?
when is <item> due?
who has <item>?
who is producer of <production>?
```

### info
Modifiers: __after__, __before__

### make group `<name>` `<item>...`
```
> @bookie make group "" 4k camera" "tripod"
```

### status

### update producers `<new_producer>` `<production>`
```
> @bookie update producers "Eric Londres" "The Egress"
Eric Londres is now the producer of The Egress.
```

### what does `<user>` have?

### what is due by `<date>`?

### when is `<item>` due?

### who has `<item>`?

### who is producer of `<production>`?

## Search modifiers
### after:`<date>`
| Arguments         | Default           | 
|-------------------|-------------------|
| `YYYY-MM-DD`, `MM-DD` | None              |
    
### before:`<date>`
| Arguments         | Default           | 
|-------------------|-------------------|
| `YYYY-MM-DD`, `MM-DD` | None              |

### format
| Arguments         | Default           |
|-------------------|-------------------|
| __spreadsheet__, None | None              |
    
If this argument is set to _spreadsheet_, then the bot will reply with a 
url to a spreadsheet where the information can be found.

### group
| Arguments            | Default |
|----------------------|---------|
| __true__, __false__, __yes__, __no__ | __true__ |

Whether to display individual items or groupings of checked out items
### share
| Arguments     | Default |
|---------------|---------|
| `@<username>` | None    |

## Technical Details
- Uses a Redis server to retain a sorted-set of checkouts by due-date timestamp

## Contact
For more information, contact `bookiebot.sittv@gmail.com`