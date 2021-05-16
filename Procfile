web: gunicorn EmplayWeb.wsgi --chdir backend --limit-request-line 8188 --log-file -
worker: REMAP_SIGTERM=SIGQUIT celery --workdir backend --app=EmplayWeb worker --loglevel=info
beat: REMAP_SIGTERM=SIGQUIT celery --workdir backend --app=EmplayWeb beat -S redbeat.RedBeatScheduler --loglevel=info
