---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: skills
    content:
      title: Skills
      text: ''
      # Choose a user to display skills from (a folder name within `content/authors/`)
      username: admin
    design:
      columns: '1'
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Adjunct Assistant Professor
          company: Hong Kong University of Science and Technology (Guangzhou)
          company_url: 'https://www.hkust-gz.edu.cn/'
          company_logo: ''
          location: Guangzhou, China
          date_start: '2024-08-01'
          date_end: ''
          description: |2-
              Thrust of Intelligent Transportation
        - title: Team Leader & Senior Researcher
          company: Lower Airspace Economy Research Institute, International Digital Economy Academy
          company_url: 'https://idea.edu.cn/'
          company_logo: ''
          location: Shenzhen, China
          date_start: '2024-01-01'
          date_end: ''
          description: |2-
              Leading a team of 10+ researchers in lower airspace economy and autonomous systems research.
        - title: Independent Researcher
          company: Beijing Jiaotong University
          company_url: ''
          company_logo: ''
          location: Beijing, China
          date_start: '2023-09-01'
          date_end: '2023-12-31'
          description: Collaborative research in computer vision and autonomous systems.
        - title: Algorithm Expert
          company: Autonomous Driving Lab, CaiNiao & DAMO Academy, Alibaba Group
          company_url: 'https://www.alibabagroup.com/'
          company_logo: ''
          location: Hangzhou, China
          date_start: '2021-12-01'
          date_end: '2023-08-31'
          description: Developed advanced algorithms for autonomous driving systems and logistics automation.
        - title: PostDoc Researcher
          company: Technical University of Denmark
          company_url: 'https://www.dtu.dk/'
          company_logo: ''
          location: Copenhagen, Denmark
          date_start: '2021-02-01'
          date_end: '2021-06-30'
          description: Research in computer vision and UAV positioning systems.
    design:
      columns: '2'
  - block: accomplishments
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Awards & Honors'
      subtitle:
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: ''
          date_end: ''
          date_start: '2026-01-01'
          description: 'Recognized for outstanding contributions to reviewing for IEEE Transactions on Instrumentation and Measurement'
          organization: IEEE Instrumentation & Measurement Society
          organization_url: https://ieee-ims.org/
          title: IEEE TIM Outstanding Reviewer
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2025-01-01'
          description: 'National talent recognition program for outstanding young researchers in China'
          organization: China Ministry
          organization_url: ''
          title: National Youth Talents Plan
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2019-01-01'
          description: 'Travel funding support for research collaboration'
          organization: Otto Mønsteds Fond
          organization_url: ''
          title: Travel Allowance
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2010-01-01'
          description: 'Provincial-level honor for academic excellence'
          organization: ShaanXi Province, China
          organization_url: ''
          title: Honor Excellent Undergraduate Students
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2009-01-01'
          description: 'National scholarship for top academic performance'
          organization: Chinese Ministry of Education
          organization_url: ''
          title: National Scholarship
          url: ''
    design:
      columns: '2'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Deep Learning
          tag: Deep Learning
        - name: Other
          tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: markdown
    content:
      title: Gallery
      subtitle: ''
      text: |-
        {{< gallery album="demo" >}}
    design:
      columns: '1'
  - block: collection
    id: featured
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card
  - block: collection
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  - block: markdown
    id: patents
    content:
      title: Patents & Book Chapters
      subtitle: ''
      text: |-
        ### Book Chapters
        - **Advance on pseudolite network selection for optimal positioning**  
          X. Hu, L. Liu, and W. Jiang  
          *Handbook of Wireless Positioning*, Springer, 2024, pp. 1–31
        
        ### Selected Patents
        - **Flight path determination**  
          L. Zhang, X. Hu, and A. Liu  
          US Patent 12,235,643, Feb. 2025
        
        - **Gimbal servo control method and control device**  
          X. Hu, G. Su, A. Liu, L. Zhang, and P. Zhaoliang  
          US Patent 12,075,159, Aug. 2024
        
        - **Systems and methods for adjusting UAV trajectory**  
          L. Zhang, X. Hu, A. Liu, and G. Zhou  
          US Patent 11,008,098, May 2021
        
        - **Systems and methods for UAV path planning and control**  
          X. Hu, A. Liu, L. Zhang, and K. Tang  
          US Patent 10,860,040, Dec. 2020
        
        *Total: 19 US/WO patents in UAV navigation, flight control, and sensor calibration*
    design:
      columns: '2'
  - block: tag_cloud
    content:
      title: Popular Topics
    design:
      columns: '2'
  - block: markdown
    id: visitor-map
    content:
      title: Visitor Map
      subtitle: 'Where our visitors come from'
      text: |-
        <div style="text-align: center; margin: 20px 0;" aria-label="Interactive visitor map showing geographic distribution of website visitors">
          <script type="text/javascript" id="clustrmaps" src="https://cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=a&t=tt&d=FQXLJzqYhZjXLhVJRTbkKQqJUjR0z7qWjUJLxbGXQfk&co=2d78ad&cmo=3acc3a&cmn=ff5353&ct=ffffff"></script>
          <noscript>
            <p>This section displays an interactive map showing the geographic distribution of our website visitors. JavaScript is required to view the map.</p>
          </noscript>
        </div>
        
        <p style="text-align: center; font-size: 0.85em; color: #666; margin-top: 10px;">
          <em>Note: This map uses ClustrMaps to collect anonymized visitor location data for analytics purposes.</em>
        </p>
    design:
      columns: '1'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Please feel free to reach out for research collaborations or inquiries.
      # Contact (add or remove contact options as necessary)
      email: hux062303@gmail.com
      phone: (+86) 18664581982
      address:
        street: ''
        city: Shenzhen
        region: Futian District
        postcode: '518000'
        country: China
        country_code: CN
      directions: ''
      office_hours: []
      contact_links: []
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---
