<template>
  <footer class="container footer">
    <div class="footer__logo">
      <img
        src="/images/logo.svg"
        alt=""
      >
    </div>
    <div class="contacts footer__contacts">
      <table>
        <tr
          v-for="contact in contacts"
          :key="contact.text"
        >
          <td class="contacts__label">
            {{ contact.label }}
          </td>
          <td class="contacts__info">
            <a
              :href="contact.link"
              target="_blank"
            >
              {{ contact.text }}
            </a>
          </td>
        </tr>
        <tr valign="top">
          <td
            valign="top"
            class="contacts__label"
            style="vertical-align: top"
          >
            App
          </td>
          <td class="contacts__info">
            <a href="">
              <img
                src="/images/App-Store-Button.svg"
                alt="app"
              >
            </a>
          </td>
        </tr>
      </table>
    </div>
    <div class="links footer__links">
      <ul>
        <li
          v-for="link in legalLinks"
          :key="link.text"
        >
          <a
            :href="link.link"
            target="_blank"
          >{{ link.text }}</a>
        </li>
      </ul>
    </div>
    <div class="copyright footer__copyright">
      <p>
        Casl Invest is a trademark of CASL LLC, <br>
        registered at Suite 305, Griffith <br>
        Corporate Centre, Beachmont, <br>
        Kingstown, St. Vincent and Grenadines
      </p>
    </div>
    <div class="footer__text text">
      <p>
        This website is intended to report solely on the investment strategies and opportunities identified by Casl Invest. Additional information is available upon request, to accredited investors only. Information herein is believed to be reliable but Casl Invest does not warrant its completeness or accuracy. Opinions and estimates constitute our judgment and are subject to change without notice. Past performance is not indicative of future results. The material is not intended as an offer or solicitation for the purchase or sale of any financial instrument. We have prepared this presentation without consideration of the investment objectives, financial situation or particular needs of any individual investor. The investments and strategies discussed herein may not be suitable for all investors. You should consider your own investment objectives, financial situation and particular needs before taking any action with respect to a financial product referred to on our website. If you have any doubts, you should consult your Casl Invest Client Advisor. The material is not intended to provide, and should not be relied on for, accounting, legal or tax advice or investment recommendations. You should consult your tax or legal advisor about the issues discussed herein.
        <br>
        This web site is issued in St. Vincent and the Grenadines by Casl LLC, registration number 2558, a company regulated by the Financial Services Authority. The company does not provide any services to citizens of the United States, Iraq, North Korea.
      </p>
    </div>
  </footer>
</template>

<script setup>
const contacts = [
	{ text: 'info@caslinvest.com', link: 'mailto:info@caslinvest.com', label: 'Email'},
	{ text: '+442045771554', link: 'tel:+442045771554', label: 'Phone'},
	{ text: '@casl_support', link: 'http://t.me/casl_support', label: 'Telegram'},
]

const legalLinks = [
	{text: 'Investment memorandum', link: ''},
	{text: 'Terms and conditions', link: '/docs/Casl_Invest_Terms_of_Use.pdf'},
	{text: 'Privacy policy', link: '/docs/Casl_Invest_PrivPolicy.pdf'},
	{text: 'KYC/AML Policy', link: '/docs/Casl_Invest_AML_policy.pdf'}
]

</script>

<style scoped lang="scss">
  .footer {
    padding-top: 308px;
    padding-bottom: 70px;

    display: grid;
    grid-template-columns: 450px 641px;
    grid-column-gap: 189px;
    grid-template-rows: auto;

    grid-template-areas:
        'logo logo'
        'contacts text'
        'links text'
        'copyright text'
    ;

    &__logo {
      margin-bottom: 38px;
      grid-area: logo;
    }
    &__contacts {
      grid-area: contacts;
    }
    &__links {
      grid-area: links;
    }
    &__copyright {
      grid-area: copyright;
    }
    &__text {
      grid-area: text;
    }
  }

  .contacts {
    padding-bottom: 21px;

    border-bottom: 2px solid $Dark-90;

    tr td:first-child {
      width: 180px;
    }

    td, td a {
      font-weight: 300;
      font-size: calc(100vw * 24px / (1440px));
      line-height: 130%;
    }
    &__label {
      color: $Dark-80;

      padding-bottom: 20px;
    }
    &__info a {
      color: $Dark-70;
      text-decoration: none;
      &:hover {
        text-decoration: underline;
      }
    }
    a {
      img {
        background: $Dark-100;

        &:hover {
          background: $Dark-90;
        }

        &:active {
          background: $Dark-80;
        }
      }
    }
  }

  .links {
    padding: 26px 0 13px;
    border-bottom: 2px solid $Dark-90;
    ul {
      li {
        margin-bottom: 20px;
        &:last-child {
          margin-bottom: 0;
        }
        a {
          font-weight: 300;
          font-size: calc(100vw * 24px / (1440px));
          line-height: 130%;

          color: $Dark-70;

          text-decoration: none;
          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }

  .copyright {
    padding: 38px 0 0 ;
    p {
      font-weight: 300;
      font-size: calc(100vw * 24px / (1440px));
      line-height: 130%;

      color: $Dark-80;
    }
  }

  .text {
    p {
      font-weight: 300;
      font-size: calc(100vw * 21px / (1440px));
      line-height: 130%;

      color: $Dark-80;
    }
  }

</style>
