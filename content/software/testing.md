Title: Testing (Software Development)
Slug: testing
Date: 2015-06-16 01:03:10
Tags: testing, pytest, presentation, software, python
Category: software
Summary: Getting familiar with testing in software industry.

The idea is here is to introduce you the world of testing in software industry and provide some guidelines and things to keep in mind while you are doing so.

<iframe src="https://docs.google.com/presentation/embed?id=1yesEE3ScAsJ3L8AkNMTvEZfOcblBkyVVu1JG0KeCG-4&amp;start=false&amp;loop=false&amp; frameborder="0" width="100%" height="378" style="border:0" allowfullscreen=true></iframe>
<a href="https://docs.google.com/presentation/d/1yesEE3ScAsJ3L8AkNMTvEZfOcblBkyVVu1JG0KeCG-4/pub" target="_blank"><small>Open in new tab</small></a>

# What is Testing?

Testing in it's very basic terms means, __"See if something is working"__ and there are many ways of doing it. Some do by trying things in a controlled environment, some do out in the world live, some ask someone else to do it for them. 

In software industry, testing almost the same thing.

# Why testing is important?

> In softwares industry, a bad code is acceptable, not a wrong code.

# When to test code?

As with anything, 

> Softwares must be tested, *as soon as possible*.

The reason being, if you don't 1) probably you'll never do it 2) the value of that test decreases as much as you delay it.

> Now is better than never.
> -- [Zen of Python, PEP20][zen]

# How to test?

> Tools are you friend when you testing something, keep them handy and sharp.

### Testing Tools

If you are able to write or speak in a particular lauguage, it become very easy to test or tell it to someone what to test. Now, if you have a better tools, it just becomes a breeze to test anything.

While testing, the tools can be categorized in two catergories:
1. Tools that help in discovering, run and cleaning up a test (pytest, unittest, nose, tox, DjangoTestRunner, etc.)
2. Tools you can use inside your test code (mock, freezegun, responses)


```shell
$ pip install pytest
```

```python
# file: my_utils.py
def is_prime(num):
    ## Do something here and return true or false
    return True


# file: test_my_utils.py
from my_utils import is_prime

def test_is_prime():
    assert is_prime(2) is True
    assert is_prime(43) is True
    assert is_prime("abc") is False
    assert is_prime(10) is False
```
```shell
$ py.test
```

# Further Reading:

1. [pytest.org][pytest]
2. [Testing Your Code - Python Guide][python-guide-testing] - by Kenneth Reitz

Got questions/suggestion, write in the comment below, if you whant to fix/improve this writeup edit it [here][edit-url] ;). 

[pytest]: http://pytest.org
[python-guide-testing]: http://docs.python-guide.org/en/latest/writing/tests/
[edit-url]: https://github.com/theskumar/blog/edit/master/content/software/testing.md
[zen]: https://www.python.org/dev/peps/pep-0020/