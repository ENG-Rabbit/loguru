.. raw:: html

    <p align="center">
        <a href="#readme">
            <img alt="Loguru logo" src="https://raw.githubusercontent.com/Delgan/loguru/master/docs/_static/img/logo.png">
            <!-- Logo credits: Sambeet from Pixaday -->
            <!-- Logo fonts: Comfortaa + Raleway -->
        </a>
    </p>
    <p align="center">
        <a href="https://pypi.python.org/pypi/loguru"><img alt="Pypi version" src="https://img.shields.io/pypi/v/loguru.svg"></a>
        <a href="https://pypi.python.org/pypi/loguru"><img alt="Python versions" src="https://img.shields.io/badge/python-3.5%2B%20%7C%20PyPy-blue.svg"></a>
        <a href="https://loguru.readthedocs.io/en/stable/index.html"><img alt="Documentation" src="https://img.shields.io/readthedocs/loguru.svg"></a>
        <a href="https://github.com/Delgan/loguru/actions/workflows/tests.yml?query=branch:master"><img alt="Build status" src="https://img.shields.io/github/workflow/status/Delgan/loguru/Tests/master"></a>
        <a href="https://codecov.io/gh/delgan/loguru/branch/master"><img alt="Coverage" src="https://img.shields.io/codecov/c/github/delgan/loguru/master.svg"></a>
        <a href="https://app.codacy.com/gh/Delgan/loguru/dashboard"><img alt="Code quality" src="https://img.shields.io/codacy/grade/be7337df3c0d40d1929eb7f79b1671a6.svg"></a>
        <a href="https://github.com/Delgan/loguru/blob/master/LICENSE"><img alt="License" src="https://img.shields.io/github/license/delgan/loguru.svg"></a>
    </p>
    <p align="center">
        <a href="#readme">
            <img alt="Loguru logo" src="https://raw.githubusercontent.com/Delgan/loguru/master/docs/_static/img/demo.gif">
        </a>
    </p>

=========

**Loguru** کتابخانه ای است که هدف آن لاگ‌گیری لذت بخش در پایتون است.

آیا تا به حال در مورد پیکربندی یک لاگر احساس تنبلی کرده اید و آیا به جای آن از ``()print`` استفاده می کنید؟ با استفاده از Loguru شما هیچ بهانه ای برای عدم استفاده از لاگر از ابتدا ندارید، این کار به سادگی ``from loguru import logger`` است.

همچنین، این کتابخانه این را نیز در نظر گرفته است تا با افزودن دسته ای از توابع مفید که اخطارهای لاگ کردن های استاندارد را حل می کند، لاگینگ پایتون را کمتر دردسرساز کند. استفاده از لاگ در برنامه شما باید خودکار باشد، **Loguru** سعی می کند آن را هم دلپذیر و هم قدرتمند کند.

.. end-of-readme-intro

نصب
------------
به همان راحتی که فکر می کنید.
::

    pip install loguru


امکانات
--------

* `Ready to use out of the box without boilerplate`_
* `No Handler, no Formatter, no Filter: one function to rule them all`_
* `Easier file logging with rotation / retention / compression`_
* `Modern string formatting using braces style`_
* `Exceptions catching within threads or main`_
* `Pretty logging with colors`_
* `Asynchronous, Thread-safe, Multiprocess-safe`_
* `Fully descriptive exceptions`_
* `Structured logging as needed`_
* `Lazy evaluation of expensive functions`_
* `Customizable levels`_
* `Better datetime handling`_
* `Suitable for scripts and libraries`_
* `Entirely compatible with standard logging`_
* `Personalizable defaults through environment variables`_
* `Convenient parser`_
* `Exhaustive notifier`_
* |strike| `10x faster than built-in logging`_ |/strike|

تور loguru گردی
-------------

.. highlight:: python3

.. |logger| replace:: ``لاگر``
.. _logger: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger

.. |add| replace:: ``()add``
.. _add: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.add

.. |حذف| replace:: حذف
.. _حذف: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.remove

.. |complete| replace:: ``complete()``
.. _complete: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.complete

.. |catch| replace:: ``()catch``
.. _catch: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.catch

.. |bind| replace:: ``bind()``
.. _bind: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.bind

.. |contextualize| replace:: ``contextualize()``
.. _contextualize: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.contextualize

.. |patch| replace:: ``patch()``
.. _patch: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.patch

.. |opt| replace:: ``opt()``
.. _opt: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.opt

.. |trace| replace:: ``trace()``
.. _trace: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.trace

.. |success| replace:: ``success()``
.. _success: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.success

.. |level| replace:: ``level()``
.. _level: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.level

.. |configure| replace:: ``configure()``
.. _configure: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.configure

.. |disable| replace:: ``disable()``
.. _disable: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.disable

.. |enable| replace:: ``enable()``
.. _enable: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.enable

.. |parse| replace:: ``parse()``
.. _parse: https://loguru.readthedocs.io/en/stable/api/logger.html#loguru._logger.Logger.parse

.. _سینک ها: https://loguru.readthedocs.io/en/stable/api/logger.html#sink
.. _گزارشی از نوع دیکشنری: https://loguru.readthedocs.io/en/stable/api/logger.html#record
.. _پیام های لاگ ها: https://loguru.readthedocs.io/en/stable/api/logger.html#message
.. _به راحتی قابل تنظیم: https://loguru.readthedocs.io/en/stable/api/logger.html#file
.. _markup tags: https://loguru.readthedocs.io/en/stable/api/logger.html#color
.. _fixes it: https://loguru.readthedocs.io/en/stable/api/logger.html#time
.. _No problem: https://loguru.readthedocs.io/en/stable/api/logger.html#env
.. _logging levels: https://loguru.readthedocs.io/en/stable/api/logger.html#levels

.. |better_exceptions| replace:: ``better_exceptions``
.. _better_exceptions: https://github.com/Qix-/better-exceptions

.. |notifiers| replace:: ``notifiers``
.. _notifiers: https://github.com/notifiers/notifiers


Ready to use out of the box without boilerplate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

مفهوم اصلی ``Loguru`` این است که **یک و تنها یک** |logger|_ وجود دارد.

برای راحتی بیشتر، از پیش پیکربندی شده است و برای شروع به صورت ``stderr`` خروجی می‌دهد (اما این کاملاً قابل تنظیم است).

::

    from loguru import logger

    logger.debug("خود خودشه، یه لاگینگ ساده و زیبا")

|logger|_ فقط یک رابط است که پیام های لاگ را به کنترل کننده های پیکربندی شده ارسال می کند. سادست، مگه نه؟


بدون نگه دارنده، قالب ساز و حتی فیلتر: یک تابع برای کنترل همه آنها
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

چگونه یک نگه دارنده اضافه کنیم؟ چگونه قالب بندی گزارش ها را تنظیم کنیم؟ چگونه پیام ها را فیلتر کنیم؟ چگونه سطح را تنظیم کنیم؟

جواب سادست با تابع |add|_ .

::

    logger.add(sys.stderr, format="{time} {level} {message}", filter="my_module", level="INFO")

این تابع برای ثبت `سینک ها`_ استفاده می شود که آنها مسئول مدیریت `پیام های لاگ ها`_ به شکل `گزارشی از نوع دیکشنری`_ هستند. یک سینک می تواند اشکال مختلفی داشته باشد: یک تابع ساده، یک رشته آدرس، یک شی فایل مانند، یک تابع موازی (coroutine) یا یک نگه دارنده داخلی.

توجه داشته باشید که شما می‌توانید با استفاده از شناسه‌ای که هنگام اضافه کردن آن بازگردانده شده است، یک نگه دارنده که قبلاً اضافه شده را |حذف|_ کنید. این به ویژه در صورتی مفید است که می‌خواهید نگه دارنده پیش‌فرض ``stderr`` را جایگزین کنید: کافیست برای شروعی تازه، ()logger.remove را فراخوانی کنید.

واقعه نگاری آسان تر درون یک فایل با rotation / retention / compression
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

اگر شما می خواهید که پیام ها را داخل فایلی لاگ نمایید فقط کافیست از رشته آدرس فایل به عنوان یک سینک استفاده نمایید. همچنین برای راحتی می توان آن را به طور خودکار زمان بندی کرد::

    logger.add("file_{time}.log")

همچنین اگر به لاگر چرخشی نیاز دارید، اگر می‌خواهید گزارش‌های قدیمی‌تر را حذف کنید، یا اگر می‌خواهید فایل‌های خود را در زمان بسته شدن فشرده کنید، `به راحتی قابل تنظیم`_ است.

::

    logger.add("file_1.log", rotation="500 MB")    # به طور خودکار فایل های بزرگ را میچرخونه
    logger.add("file_2.log", rotation="12:00")     # هر روز ظهر یه فایل جدید ایجاد میکنه
    logger.add("file_3.log", rotation="1 week")    # هر یه هفته فایل جدید ایجاد میکنه

    logger.add("file_X.log", retention="10 days")  # بعد از یه مدت فایل پاک میشه

    logger.add("file_Y.log", compression="zip")    # فضای دوست داشتنیمون رو بر می گردونه


قالب بندی مدرن رشته ها  با استفاده از سبک آکولاد
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`Loguru` از قالب بندی بسیار زیباتر و قدرتمندتر ``{}`` بیش از``%`` استفاده می کند، توابع ورود به سیستم در واقع معادل ()str.format هستند.

::

    logger.info("If you're using Python {}, prefer {feature} of course!", 3.6, feature="f-strings")


گرفتن و ثبت استثنائات داخل کد اصلی یا ریسه ها (threads)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

آیا تا به حال دیده اید که برنامه خود به طور غیرمنتظره ای از کار بیفتد بدون اینکه چیزی در فایل لاگ مشاهده کنید؟ آیا تا به حال متوجه شده اید که استثناهای رخ داده در رشته ها ثبت نشده اند؟ این را می توان با استفاده از _|catch| (به صورت دکوریتور یا داخل کد) حل کرد که تضمین می کند هر گونه خطا به درستی در |logger|_ منتشر می شود.


::

    @logger.catch
    def my_function(x, y, z):
        # An error? It's caught anyway!
        return 1 / (x + y + z)


Pretty logging with colors
^^^^^^^^^^^^^^^^^^^^^^^^^^

`Loguru` automatically adds colors to your logs if your terminal is compatible. You can define your favorite style by using `markup tags`_ in the sink format.

::

    logger.add(sys.stdout, colorize=True, format="<green>{time}</green> <level>{message}</level>")


Asynchronous, Thread-safe, Multiprocess-safe
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

All sinks added to the |logger|_ are thread-safe by default. They are not multiprocess-safe, but you can ``enqueue`` the messages to ensure logs integrity. This same argument can also be used if you want async logging.

::

    logger.add("somefile.log", enqueue=True)

Coroutine functions used as sinks are also supported and should be awaited with |complete|_.


Fully descriptive exceptions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Logging exceptions that occur in your code is important to track bugs, but it's quite useless if you don't know why it failed. `Loguru` helps you identify problems by allowing the entire stack trace to be displayed, including values of variables (thanks |better_exceptions|_ for this!).

The code::

    logger.add("out.log", backtrace=True, diagnose=True)  # Caution, may leak sensitive data in prod

    def func(a, b):
        return a / b

    def nested(c):
        try:
            func(5, c)
        except ZeroDivisionError:
            logger.exception("What?!")

    nested(0)

Would result in:

.. code-block:: none

    2018-07-17 01:38:43.975 | ERROR    | __main__:nested:10 - What?!
    Traceback (most recent call last):

      File "test.py", line 12, in <module>
        nested(0)
        └ <function nested at 0x7f5c755322f0>

    > File "test.py", line 8, in nested
        func(5, c)
        │       └ 0
        └ <function func at 0x7f5c79fc2e18>

      File "test.py", line 4, in func
        return a / b
               │   └ 0
               └ 5

    ZeroDivisionError: division by zero


Structured logging as needed
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Want your logs to be serialized for easier parsing or to pass them around? Using the ``serialize`` argument, each log message will be converted to a JSON string before being sent to the configured sink.

::

    logger.add(custom_sink_function, serialize=True)

Using |bind|_ you can contextualize your logger messages by modifying the `extra` record attribute.

::

    logger.add("file.log", format="{extra[ip]} {extra[user]} {message}")
    context_logger = logger.bind(ip="192.168.0.1", user="someone")
    context_logger.info("Contextualize your logger easily")
    context_logger.bind(user="someone_else").info("Inline binding of extra attribute")
    context_logger.info("Use kwargs to add context during formatting: {user}", user="anybody")

It is possible to modify a context-local state temporarily with |contextualize|_:

::

    with logger.contextualize(task=task_id):
        do_something()
        logger.info("End of task")

You can also have more fine-grained control over your logs by combining |bind|_ and ``filter``:

::

    logger.add("special.log", filter=lambda record: "special" in record["extra"])
    logger.debug("This message is not logged to the file")
    logger.bind(special=True).info("This message, though, is logged to the file!")

Finally, the |patch|_ method allows dynamic values to be attached to the record dict of each new message:

::

    logger.add(sys.stderr, format="{extra[utc]} {message}")
    logger = logger.patch(lambda record: record["extra"].update(utc=datetime.utcnow()))


Lazy evaluation of expensive functions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Sometime you would like to log verbose information without performance penalty in production, you can use the |opt|_ method to achieve this.

::

    logger.opt(lazy=True).debug("If sink level <= DEBUG: {x}", x=lambda: expensive_function(2**64))

    # By the way, "opt()" serves many usages
    logger.opt(exception=True).info("Error stacktrace added to the log message (tuple accepted too)")
    logger.opt(colors=True).info("Per message <blue>colors</blue>")
    logger.opt(record=True).info("Display values from the record (eg. {record[thread]})")
    logger.opt(raw=True).info("Bypass sink formatting\n")
    logger.opt(depth=1).info("Use parent stack context (useful within wrapped functions)")
    logger.opt(capture=False).info("Keyword arguments not added to {dest} dict", dest="extra")


Customizable levels
^^^^^^^^^^^^^^^^^^^

`Loguru` comes with all standard `logging levels`_ to which |trace|_ and |success|_ are added. Do you need more? Then, just create it by using the |level|_ function.

::

    new_level = logger.level("SNAKY", no=38, color="<yellow>", icon="🐍")

    logger.log("SNAKY", "Here we go!")


Better datetime handling
^^^^^^^^^^^^^^^^^^^^^^^^

The standard logging is bloated with arguments like ``datefmt`` or ``msecs``, ``%(asctime)s`` and ``%(created)s``, naive datetimes without timezone information, not intuitive formatting, etc. `Loguru` `fixes it`_:

::

    logger.add("file.log", format="{time:YYYY-MM-DD at HH:mm:ss} | {level} | {message}")


Suitable for scripts and libraries
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Using the logger in your scripts is easy, and you can |configure|_ it at start. To use `Loguru` from inside a library, remember to never call |add|_ but use |disable|_ instead so logging functions become no-op. If a developer wishes to see your library's logs, he can |enable|_ it again.

::

    # For scripts
    config = {
        "handlers": [
            {"sink": sys.stdout, "format": "{time} - {message}"},
            {"sink": "file.log", "serialize": True},
        ],
        "extra": {"user": "someone"}
    }
    logger.configure(**config)

    # For libraries
    logger.disable("my_library")
    logger.info("No matter added sinks, this message is not displayed")
    logger.enable("my_library")
    logger.info("This message however is propagated to the sinks")


Entirely compatible with standard logging
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Wish to use built-in logging ``Handler`` as a `Loguru` sink?

::

    handler = logging.handlers.SysLogHandler(address=('localhost', 514))
    logger.add(handler)

Need to propagate `Loguru` messages to standard `logging`?

::

    class PropagateHandler(logging.Handler):
        def emit(self, record):
            logging.getLogger(record.name).handle(record)

    logger.add(PropagateHandler(), format="{message}")

Want to intercept standard `logging` messages toward your `Loguru` sinks?

::

    class InterceptHandler(logging.Handler):
        def emit(self, record):
            # Get corresponding Loguru level if it exists
            try:
                level = logger.level(record.levelname).name
            except ValueError:
                level = record.levelno

            # Find caller from where originated the logged message
            frame, depth = logging.currentframe(), 2
            while frame.f_code.co_filename == logging.__file__:
                frame = frame.f_back
                depth += 1

            logger.opt(depth=depth, exception=record.exc_info).log(level, record.getMessage())

    logging.basicConfig(handlers=[InterceptHandler()], level=0)


Personalizable defaults through environment variables
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Don't like the default logger formatting? Would prefer another ``DEBUG`` color? `No problem`_::

    # Linux / OSX
    export LOGURU_FORMAT="{time} | <lvl>{message}</lvl>"

    # Windows
    setx LOGURU_DEBUG_COLOR "<green>"


Convenient parser
^^^^^^^^^^^^^^^^^

It is often useful to extract specific information from generated logs, this is why `Loguru` provides a |parse|_ method which helps to deal with logs and regexes.

::

    pattern = r"(?P<time>.*) - (?P<level>[0-9]+) - (?P<message>.*)"  # Regex with named groups
    caster_dict = dict(time=dateutil.parser.parse, level=int)        # Transform matching groups

    for groups in logger.parse("file.log", pattern, cast=caster_dict):
        print("Parsed:", groups)
        # {"level": 30, "message": "Log example", "time": datetime(2018, 12, 09, 11, 23, 55)}


Exhaustive notifier
^^^^^^^^^^^^^^^^^^^

`Loguru` can easily be combined with the great |notifiers|_ library (must be installed separately) to receive an e-mail when your program fail unexpectedly or to send many other kind of notifications.

::

    import notifiers

    params = {
        "username": "you@gmail.com",
        "password": "abc123",
        "to": "dest@gmail.com"
    }

    # Send a single notification
    notifier = notifiers.get_notifier("gmail")
    notifier.notify(message="The application is running!", **params)

    # Be alerted on each error message
    from notifiers.logging import NotificationHandler

    handler = NotificationHandler("gmail", defaults=params)
    logger.add(handler, level="ERROR")


|strike|

10x faster than built-in logging
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|/strike|

Although logging impact on performances is in most cases negligible, a zero-cost logger would allow to use it anywhere without much concern. In an upcoming release, Loguru's critical functions will be implemented in C for maximum speed.


.. |strike| raw:: html

   <strike>

.. |/strike| raw:: html

   </strike>

.. end-of-readme-usage


Documentation
-------------

* `API Reference <https://loguru.readthedocs.io/en/stable/api/logger.html>`_
* `Help & Guides <https://loguru.readthedocs.io/en/stable/resources.html>`_
* `Type hints <https://loguru.readthedocs.io/en/stable/api/type_hints.html>`_
* `Contributing <https://loguru.readthedocs.io/en/stable/project/contributing.html>`_
* `License <https://loguru.readthedocs.io/en/stable/project/license.html>`_
* `Changelog <https://loguru.readthedocs.io/en/stable/project/changelog.html>`_
