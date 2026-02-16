You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-group-company.html",
    "context": {
      "title": "FYNAMICS | Group Company",
      "first_heading": "FAMILY"
    }
  },
  {
    "path": "apply-now.html",
    "context": {
      "title": "FYNAMICS | Apply",
      "first_heading": "APPLY"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "JIL | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/614da49ccb4f3fae8d700f8236e5531a.css",
    "context": {
      "path": "css/614da49ccb4f3fae8d700f8236e5531a.css"
    }
  },
  {
    "path": "css/827fd34f9214e869c8b614f913aef7d5.css",
    "context": {
      "path": "css/827fd34f9214e869c8b614f913aef7d5.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "gold-loan.html",
    "context": {
      "title": "JIL | Gold Loan",
      "first_heading": "GOLD LOAN"
    }
  },
  {
    "path": "imgs/05d90fde3555bf2062cf22fceeff0423.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Values",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09e5c07fb312483917f6444c939f219d.webp",
    "context": {
      "refs": [
        {
          "alt": "Jil Website",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/14f86e0fbf86e7a4c0fe4dc5d7e95b7b.webp",
    "context": {
      "refs": [
        {
          "alt": "Personal Loan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a6de018e25052e5ab295047be46f1a7.webp",
    "context": {
      "refs": [
        {
          "alt": "Amar Singh Jadon",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2041137c7f382dc06a3adc882b6008db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/317e131bbbe5192bd659d55126abac3c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c45af120c60d4847fa4c4e8d520796e.webp",
    "context": {
      "refs": [
        {
          "alt": "We have strategically planned to cover Northern India in Phase 1, covering 21 locations in 6 States ",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51e89d94c2f61332aa5c729e83af701c.webp",
    "context": {
      "refs": [
        {
          "alt": "Complete OUT of the BOX style of Credit appraisal with Professionals manoeuvring their vintage pragm",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/52b14ed11310a15f3bdc5e6593c33c25.webp",
    "context": {
      "refs": [
        {
          "alt": "Documentation",
          "title": ""
        },
        {
          "alt": "Documentation",
          "title": ""
        },
        {
          "alt": "Documentation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5531ef90535a4f662e8e5033b1ea1374.webp",
    "context": {
      "refs": [
        {
          "alt": "Product",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6094bee76ebf0e27f81b0fa18e26490e.webp",
    "context": {
      "refs": [
        {
          "alt": "CA Deepak srivastava",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6116b70db19c335dd2f120cc8e904cce.webp",
    "context": {
      "refs": [
        {
          "alt": "Unsecured business loans and Loan against property",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65085863c11bcf9e386980cb9627e4a4.webp",
    "context": {
      "refs": [
        {
          "alt": "Prakash Bisht",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65bfd7d3459910f0df5cfe4071fafe39.webp",
    "context": {
      "refs": [
        {
          "alt": "Manvendra kumar",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66eb8fdd23f7df181895f0e170867978.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68a81b0c30a3852741efe30530b2db0a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6aa51577d1d6b526628261a3e3bbc902.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f32589c46d855ec487d582b54c0b670.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d32629e8f04f29bed3138d7ce8081a2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ffc9e741e439e768d2291c833d36f68.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83b3caaeb019af2028b756a279c77216.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8424490511d7d6057d85d80c47ea59ed.webp",
    "context": {
      "refs": [
        {
          "alt": "Gold Loan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/884e22354172042c8667b61d4f1fedce.webp",
    "context": {
      "refs": [
        {
          "alt": "Contact",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f4d786e19b46ae3223b8ebad90c1f1e.webp",
    "context": {
      "refs": [
        {
          "alt": "Product",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/918b326853bf701f1d86e8bf20e56fed.webp",
    "context": {
      "refs": [
        {
          "alt": "List of accepted collateral",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91e3ef2aa8da75aab7700e9d910d6af0.webp",
    "context": {
      "refs": [
        {
          "alt": "Apply",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/950e8f763450e1cdfd021484e15a287d.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa8fd8cb804409d99d0824f1f1db18c3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae49712cd42ea20bdede7b4cdebaa8a5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0f314bb953fc1855eca43c9402198cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2414c997bdd308b37057a0640b3cc3d.webp",
    "context": {
      "refs": [
        {
          "alt": "Sandeep Jadon",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b3a07c286137592e87ac487da7f9eff2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9e91b928d97d0a6f1cc08a3aaf5716c.webp",
    "context": {
      "refs": [
        {
          "alt": "FYNAMICS is an \u201cSME financing platform\u201d, with a belief that every customer is different and so are t",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc59fc771a7ab7c776de640e3ce985b6.webp",
    "context": {
      "refs": [
        {
          "alt": "Creating professional and friendly environment for Team workers.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c00a9ba0308e26548b0a04d1d329ccea.webp",
    "context": {
      "refs": [
        {
          "alt": "Product",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c235ca020a4ad1a1f976a9e72d1f1137.webp",
    "context": {
      "refs": [
        {
          "alt": "Parveen Jadon-",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c5b2f769179159bac179dce529aeab59.webp",
    "context": {
      "refs": [
        {
          "alt": "LOAN ELIGIBILITY",
          "title": ""
        },
        {
          "alt": "LOAN ELIGIBILITY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2100c6025e1de3167ef54626b262e5a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/d3fe8921a0c67b890da7ba9e5b678f82.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dee3a5eded8c50e7ba81428006182437.webp",
    "context": {
      "refs": [
        {
          "alt": "JIL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e0204b06bd8be28dc150409278a81f9e.webp",
    "context": {
      "refs": [
        {
          "alt": "Mrinal Lalchandani",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4004cc480cb910c1749643553e5a6d0.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eaf5093582920db0fac70d7aefaeed62.webp",
    "context": {
      "refs": [
        {
          "alt": "Johal Investment limited",
          "title": ""
        },
        {
          "alt": "Johal Investment limited",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fac52fc9cb80feff13775d3a756d13a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ffcc043e264bb136554e9dae8a96ff46.webp",
    "context": {
      "refs": [
        {
          "alt": "CA Ashish Sharma",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "JIL | Retail Lending Platform",
      "first_heading": "JIL"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/f9cb28192ac6299a4d01abd84088b6c3.js",
    "context": {
      "path": "js/f9cb28192ac6299a4d01abd84088b6c3.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "key-strategies.html",
    "context": {
      "title": "JIL | Key Strategies",
      "first_heading": "KEY STRATEGIES\u201cThe essence of strategy is choosing what not to do\u201d- Michael Porter"
    }
  },
  {
    "path": "our-future-plans.html",
    "context": {
      "title": "JIL | Our Future Plans",
      "first_heading": "OUR FUTURE PLANS\u201cThe best way to predict your future is to create it\u201d\u2013 Abraham Lincoln"
    }
  },
  {
    "path": "our-team.html",
    "context": {
      "title": "JIL | Our Family",
      "first_heading": "OUR FAMILY"
    }
  },
  {
    "path": "our-values.html",
    "context": {
      "title": "JIL | Our Values",
      "first_heading": "PURSUE EXCELLENCE AND SUCCESS WOULD FOLLOW"
    }
  },
  {
    "path": "personal-loan.html",
    "context": {
      "title": "JIL | Personal Loan",
      "first_heading": "PERSONAL LOAN"
    }
  },
  {
    "path": "the-real-business.html",
    "context": {
      "title": "JIL | The Real Business",
      "first_heading": "THE REAL BUSINESS\u201cAlways deliver more than expected\u201d- Larry Page"
    }
  },
  {
    "path": "unsecured-loans.html",
    "context": {
      "title": "JIL | Unsecured Business Loan",
      "first_heading": "UNSECURED BUSINESS LOANS AND LOAN AGAINST PROPERTY"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.