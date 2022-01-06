# Updating Website

## Adding/Removing lab members.

To add a member, edit the `_data/lab_members.yml` file. It should look like this:
```
members:
- name: Name1
  title: Principal Investigator
  mail: name1@cshl.edu
  twitter: name1_twitter
  linkedin: name1_lk
  summary: "Name1 is an amazing researcher"
  image: Corina_headshot.jpeg
- name: name2
  title: title_2
  mail: name2@cshl.edu
  twitter: name_2_twitter
  linkedin: name_2_lk
  summary: "name 2 is a great person."
  image: Corina_headshot.jpeg
```

To add a lab member, add a new block and edit it according to the data required:
- `name`: The name of the lab member
- `title`: Their title within the lab
- `mail`: Their work email
- `twitter`: The Twitter handle of the user. If they don't have one, remove this line.
  - This should be what's after `twitter.com/` in their profile. I.e., if the profile link is https://twitter.com/user_handle_1234, then it should only be `user_handle_1234`.
- `linkedin`: The LinkedIn profile link. If they don't have one, remove this line.
  - This should be what's after `linkedin.com/in/` in their profile. I.e., if the profile link is https://www.linkedin.com/in/user_handle_1234/, then it should only be `user_handle_1234`.
- `summary`: A summary of the lab member's CV and accomplishments, areas of research, etc.
- `image`: The name of the file with the lab member's picture, which should be in the `img` folder.

To remove a lab member from the website, simply remove the whole block for that user. Optionally, you can also delete the picture associated to that user in the `img` folder.

## Adding papers

To add a paper, you'll have to modify the `_data/publications.yml` file.

```
years:
  - year: 
      number: 2020
      publications:
          - title: "paper 1"
            link: https://www.nature.com/articles/s41586-020-2403-9
            authors: [Amor C*, Feucht J*, Leibold J*, Ho Y, Zhu C, Alonso-Curbelo D, Mansilla-Soto J, Boyer J.A, Li X, Giavridis T, Kulick A, Houlihan S, Peerschke E, Friedman S.L, Ponomarev V, Piersigili A, Sadelain M, Lowe S.W.]
            lab_members: [Amor C*]
            journal: "Nature"
            paper_info: "2020 Jun 17; 583; 127-132"
            other: "News & Views by Wagner, V and Gil J."
          - title: "paper 2"
            link: https://pubmed.ncbi.nlm.nih.gov/32376773/
            authors: [Leibold J, Ruscetti M, Cao Z, Ho Y, Baslan T, Zhou M, Abida W, Feucht J, Han T, Barriga F.M, Tsanov K.M, Zamechek-Slain L, Kulick A, Amor C, Tian S, Rybczyk Kataryna, Salgado N.R, Sanchez-Rivera F.J, Watson P.A, Stanchina E, Wilkinson J.E, Dow L.E, Abate-Shen C, Sawyers C.L., Lowe, S.W.]
            lab_members: ["Amor C"]
            journal: "Cancer Discovery"
            paper_info: "2020 Jul;10; 1038-1057"
  - year: 
      number: 2014
      publications:
          - title: "paper 3"
            link: https://pubmed.ncbi.nlm.nih.gov/25483776/
            authors: [Meng F, Du Z, Federation A, Hu J, Wang Q, Kieffer-Kwon K, Meyers RM, Amor C, Wasserman C, Neuberg D, Nussenzweig MC, Casellas R, Bradner JE, Liu XS, Alt FW.]
            lab_members: ["Amor C"]
            journal: "Cell"
            paper_info: "2014 Dec 18;159; 1538-1548"
```

If the paper is from an already existing year, add an extra `- title` block. If it's a year that is not already added, add the following at the top of the file:
```
- year:
    number: 2022
    publications:
    
```

The fields are described as follows:
- `title`: Title of the paper, as it appears in the journal
- `link`: Link to the article.
- `authors`: Listed as `[author1, author2, author3, author4,...]`. Should contain all the authors in the paper, ideally in the order listed in the paper.
- `lab_members`: Should be written as `["lab_member_1", "lab_member_2"]`. The names should match the ones in the `authors` list exactly, and will be in **bold** when listing the authors in the website, to identify whom was involved in them from the lab.
- `journal`: Name of the journal where the article was published in.
- `paper_info`: Information of the paper.
- `other`: Optional field for any other thing that need to be expressed about the paper.
