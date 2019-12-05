Title:  Extract a Piece of a Date

Tags:   Foundation, date

Link:   https://developer.apple.com/documentation/foundation/nscalendar

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: NSCalendar

Date:   21 Oct 2019

Author: Herb Bowie

Index:  date

Code: 

let now = Date()
let gregCalendar = Calendar(identifier: .gregorian)
let year = gregCalendar.component(.year, from: now)
let month = gregCalendar.component(.month, from: now)
let day = gregCalendar.component(.day, from: now)
let dayOfWeek = gregCalendar.component(.weekday, from: now)


Body: 

You need to pass the desired date to a Calendar instance and indicate which component you're interested in. 
