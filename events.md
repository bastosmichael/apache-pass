---
title: Rally Schedule
layout: events
description: Trump Train MAGA Rally Schedule of Events
intro_image: "images/features/map.jpeg"
intro_image_absolute: true
intro_image_hide_on_mobile: false
---

# Trump Train MAGA Rally Schedule

Join us for an action-packed day of patriotism, inspiring speeches, and family-friendly activities. Our Trump Train MAGA Rally features a caravan across 4 counties, culminating in a grand event at Apache Pass Camp Grounds.

## Caravan Schedule

- 8:00 AM - Caravan Check-in and Assembly (Location TBA)
- 9:00 AM - Caravan Departs
- 11:00 AM - Pit Stop 1: [County Name] (15-minute break)
- 1:00 PM - Pit Stop 2: [County Name] (Lunch break, 45 minutes)
- 3:00 PM - Pit Stop 3: [County Name] (15-minute break)
- 5:00 PM - Arrival at Apache Pass Camp Grounds, Milam County

## Main Event Schedule

- 5:00 PM - 6:30 PM: Arrival and Camp Setup
- 6:30 PM - 7:00 PM: Opening Ceremony and Pledge of Allegiance
- 7:00 PM - 8:00 PM: Dinner and Live Music
- 8:00 PM - 9:30 PM: Main Stage Speeches
  - 8:00 PM - Local Republican Party Representative
  - 8:20 PM - State Senator [Name]
  - 8:40 PM - Congressman [Name]
  - 9:00 PM - Texas Agriculture Commissioner Sid Miller
- 9:30 PM - 10:00 PM: Closing Remarks and Fireworks Display

## Day 2 Schedule (Optional for Campers)

- 7:00 AM - 9:00 AM: Breakfast (available for purchase)
- 9:00 AM - 11:00 AM: Morning Prayer and Gospel Music
- 11:00 AM - 1:00 PM: Second Amendment Celebration and Gun Safety Demonstration
- 1:00 PM - 3:00 PM: Family-Friendly Activities and Games
- 3:00 PM - Event Conclusion and Departure

Don't miss this incredible opportunity to show your support for Donald Trump and connect with fellow patriots. [Register now](/contact/) to secure your spot in the Trump Train MAGA Rally!

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "itemListElement": [
    {% for event in site.events %}
    {
      "@type": "ListItem",
      "position": {{ forloop.index }},
      "item": {
        "@type": "Event",
        "name": "{{ event.title }}",
        "description": "{{ event.description | strip_html | strip_newlines | truncate: 160 }}",
        "startDate": "{{ event.date | date_to_xmlschema }}",
        "location": {
          "@type": "Place",
          "name": "{{ event.location }}"
        },
        "organizer": {
          "@type": "Organization",
          "name": "Trump Train MAGA Rally"
        },
        "url": "{{ site.url }}{{ event.url }}"
      }
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ]
}
</script>
