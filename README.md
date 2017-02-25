ARMful Docker image with python3 preinstalled.
=========================

[![licence badge]][licence]


# Supported tags and respective Dockerfile links

- 3.5.2-r2, latest (stable/Dockerfile)
- edge-3.6.0-r0 (edge/Dockerfile)

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