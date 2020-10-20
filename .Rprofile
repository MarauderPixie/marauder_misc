## Print this on start so I know it's loaded.
## cat("Loading custom .Rprofile")

### install ddateR when not already installed:
# if (!("ddateR" %in% installed.packages())) {
#   devtools::install_github("MarauderPixie/ddateR")
# }

### Misc options
options(stringsAsFactors = FALSE, encoding = "UTF-8")


### Prompt
if (Sys.info()[1] == "Windows") {
  options(prompt = sample(c("¤ ", "× ", "‡ ", "» "), 1),
          continue = "   ¬ ")
} else {
  # options(prompt = sample(c("☉ ", "♫ ", "⚒ ", "⚙ ", "ⱺ "), 1),
  #         continue = "   ↳ ")
  options(prompt = sample(c("🌀 ", "🎵 ", "🛠 ", "🔧 ", "🗝 "), 1),
          continue = "   🔹 ")
}


### Startup
startup <- function(){
  version     <- R.Version()
  # date_string <- format(Sys.Date(), "%A, der %d. %B %Y")
  ddate       <- ddateR::ddate()

  # msg <- paste0("Oh hello! Great to see you again!\n",
  #               ddate, "\n\n",
  #               "You're working with ", version$nickname, ". Let's crunch some numbers!")
  
  # msg <- paste0(crayon::blue$bold("                         Hoi Chummer!\n\n"),
  #               ddate, "\n\n",
  #               "     Current flavor of the month is ", crayon::bold(version$nickname), ".\n",
  #                           "               Time to jack in and slice some IC.")
  
  msg <- paste0(crayon::col_align(crayon::cyan$bold("Hoi Chummer! 🖐"), nchar(ddate), "center"),
                "\n\n", ddate, "\n\n",
                crayon::col_align(paste0("Current flavor of the month is ", crayon::bold(version$nickname)), nchar(ddate), "center"), "\n",
                crayon::col_align("💢 Time to jack in and slice some IC 💢", nchar(ddate), "center"))

  cat("\f", msg, "\n\n", sep = "")
}

startup()
rm(startup)


### Packages
# suppressPackageStartupMessages(library("devtools"))
suppressPackageStartupMessages(library("ddateR"))

