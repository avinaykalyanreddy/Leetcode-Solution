
### sending mail to users using flask_mail module import Mail class and pass the object Flask(__name__)

* note dont pass password directly

```python

import getpass

from flask import *
from flask_mail import *

app = Flask(__name__)
app.config['MAIL_SERVER'] = 'smtp-mail.outlook.com'
app.config['MAIL_PORT'] = 587 # Use 465 for SSL or 587 for TLS
app.config['MAIL_USERNAME'] = 'godsons12072004@outlook.com'
app.config['MAIL_PASSWORD'] = getpass.getpass("Enter password: ")
app.config['MAIL_USE_TLS'] = True
app.config['MAIL_USE_SSL'] = False

mail = Mail(app)

@app.route("/")
def home():

  mail.send_message(  
        subject='Hello from Flask-Mail',
        sender='godsons12072004@outlook.com',
        recipients=['avinaykalyanreddy@gmail.com'],
        body="This is a test email using send_message."
  )
 """
or
    msg = Message('Hello', sender='godsons12072004@outlook.com', recipients=['avinaykalyan@gmail.com'])
    msg.body = "Hello Flask message sent from Flask-Mail"
    

    # Send email
    mail.send(msg)
    return "Sent"

"""

  return "Email sent!"
if __name__ == '__main__':
    app.run(debug=True)
```
