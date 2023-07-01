# Bobby Ressnowski, or whatever you wanna call me
personal website

i'm not so sure what i'm doing here but i'm hoping to turn this into a personal website. stay tuned or whatever


<form name="sentMessage" id="contactForm" novalidate>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Name</label>
          <input type="text" class="form-control" placeholder="Name" id="name" required data-validation-required-message="Please enter your name.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Email Address</label>
          <input type="email" class="form-control" placeholder="Email Address" id="email" required data-validation-required-message="Please enter your email address.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group col-xs-12 floating-label-form-group controls">
          <label>Phone Number</label>
          <input type="tel" class="form-control" placeholder="Phone Number" id="phone" required data-validation-required-message="Please enter your phone number.">
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <div class="control-group">
        <div class="form-group floating-label-form-group controls">
          <label>Message</label>
          <textarea rows="5" class="form-control" placeholder="Message" id="message" required data-validation-required-message="Please enter a message."></textarea>
          <p class="help-block text-danger"></p>
        </div>
      </div>
      <br>
      <div id="success"></div>
      <div class="form-group">
        <button type="submit" class="btn btn-primary" id="sendMessageButton">Send</button>
      </div>
    </form>


% if page.background %}
{% else %}
{% endif %}
{{ site.title }}
{% if site.description %} {{ site.description }} {% endif %}
{{ content }} {% for post in site.posts limit : 5 %}
{{ post.title }}
{% if post.subtitle %}
{{ post.subtitle }}
{% else %}
{{ post.excerpt | strip_html | truncatewords: 15 }}
{% endif %}
Posted by {% if post.author %} {{ post.author }} {% else %} {{ site.author }} {% endif %} on {{ post.date | date: '%B %d, %Y' }} · {% include read_time.html content=post.content %}

{% endfor %}
View All Posts →
