# My name: Kozel Maksim 

***

### Contact Information:
    - Email: makskozel84@gmail.com
    - Discord: on_samai
    - GitHub: buzzer2001

***

### Education:
    - Baranovichi State University (profession software engineer)

***

### Brief Self-Introduction:
*Now my goal is to successfully complete the course. With the help of the acquired knowledge, change the place of work.*

***

### Skills:
    - Python (Django)
    - SQL
    - HTML 
    - CSS 
    - Java (basic), C++ (basic), Javascript (basic), C# (basic)
    - Git, Github
    - PyCharm, SQLite, PostrgreSQL, MySQL, VSCode, Visual Studio,  IntelliJ IDEA

***

### Code Examples
```
class Post(models.Model):

    class Status(models.TextChoices):
        DRAFT = 'DF', 'Draft'
        PUBLISHED = 'PB', 'Published'

    title = models.CharField(max_length=250)
    slug = models.SlugField(max_length=250)
    author = models.ForeignKey(User,
                               on_delete=models.CASCADE,
                               related_name='blog_posts')
    body = models.TextField()
    publish = models.DateField(default=timezone.now)
    created = models.DateField(auto_now=True)
    updated = models.DateField(auto_now=True)
    status = models.CharField(max_length=2,
                              choices=Status.choices,
                              default=Status.DRAFT)

    objects = models.Manager()
    published = PublishedManager()

    class Meta:
        ordering = ['-publish']
        indexes = [
            models.Index(fields=['-publish']),
        ]

    def __str__(self):
        return self.title
```

***

### Work Experience:
*Now I work as a programmer at the factory.*

***

### Languages
    - English (A1)
    - Russian
    - Belarusian
