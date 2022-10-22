# libraries that are needed in this course.
libs <- c(
  "utils",
  "tidyverse",
  "googlesheets4",
  "readxl",
  "devtools",
  "plotly"
)

# define function
# if already installed, do import only.
# if not installed, do install and import.
requireLibs <- function(libs) {
  for(lib in libs) {
    if(!lib %in% library()$results[,c(1)]) {
      print(lib)
      install.packages(lib, repos="https://cran.ism.ac.jp/")
    }
    require(lib, character.only = T)
  }
}

# import libraries
requireLibs(libs)

# put messages into console
message("Successfully installed packages below...")
message("----------------------")
message(paste(libs[-1], collapse = " / "))
message("----------------------")
message("Let's enjoy Data-Science course !")


# define rendering function
render_this <- function(){
  bookdown::render_book("index.Rmd", "bookdown::gitbook")
} 

publish_this <- function(name) {
  publish_book(name = name, account = NULL, server = NULL,render = c("none", "local", "server"))
}
