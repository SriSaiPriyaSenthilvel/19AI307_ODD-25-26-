# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:

To implement the Memento Design Pattern that allows saving and restoring versions of an Article object.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create ArticleMemento to store article content (state).
4.	Create Article (Originator) that can write, save, and restore content.
5.	Create VersionHistory (Caretaker) to store multiple mementos.
6.	Allow the user to:
7.	Write new content
8.	Save current version
9.	View all saved versions
10.	Restore any version
11.	Display restored version content.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103 
*/
```

## SOURCE CODE:
```

import java.util.*;

class Article {
    private String content;

    public Article(String content) {
        this.content = content;
    }

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    // Save current state to memento
    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    // Restore state from memento
    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }

    public List<ArticleMemento> getAllVersions() {
        return versions;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read number of versions
        int n = Integer.parseInt(sc.nextLine());
        ArticleHistory history = new ArticleHistory();
        Article article = new Article("");

        // Read and save each version
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        // Read version index to restore (0-based)
        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento memento = history.getVersion(restoreIndex);
        if (memento != null) {
            article.restore(memento);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}

```
## OUTPUT:

<img width="798" height="567" alt="image" src="https://github.com/user-attachments/assets/8eb197c0-5dec-4cdd-bde8-e63832049785" />

## RESULT:

The program has been executed successfully and the output has been obtained.
