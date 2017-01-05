ARMful Docker image with python3 preinstalled.
=========================

[![licence badge]][licence]

# Build Details

- [Source Repository](https://github.com/mmorita44/arm-python3)
- [Dockerfile](https://github.com/mmorita44/arm-python3/blob/master/Dockerfile)

# Usage

Deploy python3 application with Docker.

```
FROM mmorita44:arm-python3

RUN pip3 install Flask

RUN echo -e 'from flask import Flask\napp = Flask(__name__)\n\n@app.route("/")\ndef hello():\n    return "Hello World!"\n\nif __name__ == "__main__":\n    app.run()\n' > hello.py

EXPOSE 80

CMD ["python3", "hello.py"]
```

[licence]: <LICENSE>
[licence badge]: http://img.shields.io/badge/license-MIT-blue.svg?style=flat