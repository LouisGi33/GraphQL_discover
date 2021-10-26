# GraphQL_discover
Petit test de GraphQL avec query et mutations


### Requetes QraphQL pour avoir la liste des courses contenant une certaine string dans leur titre et pouvoir en ajouter

 ```
query getCoursesWitnInTitle($title: String){
  WithInTitle: coursesWithInTitle(title: $title) {
      ... courseFields
    }
}

mutation addCourse($title: String!, $topic: String!, $author: String!, $description: String!, $url: String!) {
  addCourse(title: $title, topic: $topic, author: $author, description: $description, url: $url) {
    ... courseFields
  }
}

fragment courseFields on Course {
  title
  author
  description
  topic
  url
}
 ```
