---
title: Certificates
icon: fas fa-certificate
order: 2
layout: page
---

{% assign certificates = site.data.certificates %}
{% assign types = certificates | map: 'type' | uniq %}

{% for type in types %}
  <h2 class="mt-5 mb-4">{{ type | capitalize }}</h2>
  <div class="row row-cols-1 g-4">
    {% assign certs_by_type = certificates | where: 'type', type %}
    {% for cert in certs_by_type %}
      <div class="col">
        <div class="card h-100 hover-effect">
          <div class="card-img-top p-3 d-flex align-items-center justify-content-center">
            {% if cert.image %}
              <img src="{{ cert.image | relative_url }}" class="img-fluid rounded" alt="{{ cert.name }}" style="max-height: 500px; width: auto; object-fit: contain;">
            {% else %}
              <i class="fas fa-certificate fa-5x text-muted"></i>
            {% endif %}
          </div>
          <div class="card-body text-center">
            <h5 class="card-title" title="{{ cert.name }}">
              <a href="{{ cert.url }}" target="_blank" rel="noopener noreferrer" class="text-decoration-none text-reset stretched-link">
                {{ cert.name }}
              </a>
            </h5>
            <p class="card-text text-muted mb-1">
              <i class="far fa-building me-1"></i> {{ cert.issuer }}
            </p>
            <p class="card-text small text-muted">
              <i class="far fa-calendar-alt me-1"></i> {{ cert.date | date: "%b %d, %Y" }}
            </p>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
{% endfor %}
