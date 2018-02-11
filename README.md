# Programming-assignment-3

best <- function(state, outcome) {
  outcomeFile <- read.csv("outcome-of-care-measures.csv", colClasses = "character")
  if(outcome == "heart attack") {
    outcomeFile[, 11] <- as.numeric(outcomeFile[, 11])
    outcomeLower11 <- min(outcomeFile[, 11], na.rm = TRUE) ##minimum heart attack
    hospital11 <- outcomeFile[outcomeLower11, 2]
    return(hospital11)
  } else if(outcome == "heart failure") {
    outcomeFile[, 17] <- as.numeric(outcomeFile[, 17])
    outcomeLower17 <- min(outcomeFile[, 17], na.rm = TRUE) ##minimum heart failure
    hospital17 <- outcomeFile[outcomeLower17, 2]
    return(hospital17)
  } else if(outcome == "pneumonia") {
    outcomeFile[, 23] <- as.numeric(outcomeFile[, 23])
    outcomeLower23 <- min(outcomeFile[, 23], na.rm = TRUE) ##minimum heart failure
    hospital23 <- outcomeFile[outcomeLower23, 2]
    return(hospital23)
  }
}
