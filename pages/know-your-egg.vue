<template>
<div class="row pb-5">
  <h1 class="col-12 pt-5 pb-2">Know Your Egg</h1>
  <p class="lead col-12 pb-5">What do all those carton labels really mean? Click on each term for an explanation.</p>

  <!-- Adding accordion -->
  <div id="accordion" class="col-lg-10 col-md-10 col-sm-12" v-for="term in terms" v-bind:key="term.title">
      <div class="card">
        <div class="card-header pt-0 pb-0" id="termTitle">
          <h3 class="m-0 p-0">
            <button class="btn" data-toggle="collapse" data-target="#collapseTitle" aria-expanded="false" aria-controls="collapseTitle">{{term.title}}</button>
          </h3>
        </div>
      </div>

      <div id="collapseTitle" class="collapse" aria-labelledby="term" data-parent="#accordion">
        <div class="card-body">
          <p>{{term.def}}</p>
        </div>
      </div>
    </div>
  <!-- End accordion -->

  <p class="col-lg-10 col-md-10 col-sm-12 pt-5"><small><b>SOURCE:</b></small><br>
    <a id="content-link" href="https://www.aspca.org/">ASPCA</a>, <a id="content-link" href="https://www.aspca.org/shopwithyourheart/consumer-resources/meat-eggs-and-dairy-label-guide" target="_blank">
    Meat, Eggs and Dairy Label Guide</a></p>
    <p class="col-lg-10 col-md-10 col-sm-12">See a comparison of labels here: <br>
      <a id="content-link" href="https://www.aspca.org/shopwithyourheart/consumer-resources/meat-eggs-and-dairy-label-guide/understanding-egg-labels?ms=so_def_shareable-take-action-egg-label-guide-20170516&initialms=so_def_shareable-take-action-egg-label-guide-20170516&utm_medium=social&utm_campaign=shareable&utm_source=take-action-egg-label-guide-20170516"
    target="_blank">Understanding Egg Labels</a>
  </p>
</div>
</template>


<script>
export default {
  name: '#accordion',
  data () {
    return {
      terms: [
        {title: "CAGE-FREE",
        // Use a backslash after lines of text so Javascript knows the string is continued; otherwise, errors occur
          def: "\“Cage-free\” claims ensure that cages are prohibited, though they \
          provide no other specifications or requirements on how to rear hens more humanely. \
          For egg products from hens who are reared in cage-free environments with more \
          space, necessary enrichment like perches and nests, and, in some cases, outdoor \
          or pasture access, look for one of the ASPCA-recommended certifications below. \
          NOTE: Chickens and turkeys raised for meat (as opposed to eggs) are not typically \
          caged, rendering a cage-free label meaningless on poultry meat products."
          },
        {title: "FREE-RANGE",
          def: "Most farm animals are housed entirely indoors. The USDA requires \
          producers using “free-range” or “free-roaming” claims to demonstrate that \
          animals have “access to the outdoors,” but size, quality and length of access \
          to that outdoor space is unregulated, so conditions vary greatly and are \
          often subpar. For products from animals raised outdoors with adequate space, \
          look for Animal Welfare Approved, Global Animal Partnership (Step 3 and above) \
          or Certified Humane egg/poultry products that also say “free-range."
          },
        {title: "USDA ORGANIC",
          def: "An organic certification program that requires outdoor access for animals, \
          but does not properly enforce that requirement, and is available to farms of all \
          sizes and structures. Added hormones and subtherapeutic antibiotics are prohibited. \
          Compliance is verified by auditors on every farm every 12 months, but enforcement of \
          key standards, such as outdoor access, varies widely. Claims to require outdoor \
          access, but space, duration and quality of that access is not defined and varies \
          widely between farms. (For example, access to screened-in porches on hard, concrete \
          flooring qualifies as “outdoor access” for egg-laying hens.) Does not prohibit \
          feedlots, cage-confinement, set minimum space standards or require enrichments when \
          animals are indoors. Standards do not extended to breeding animals, transport or \
          slaughter, nor do they ensure higher-welfare breeds for animals."
          },
        {title: "CERTIFIED HUMANE",
          def: "An animal welfare certification program that includes both enriched indoor \
          and free-range/pasture-based standards, available to farms of all sizes and structures.\
          Requires continuous outdoor access for ruminants (cows, goats, sheep). If animals are \
          raised indoors, more space, bedding and enrichment are required than is typical on \
          conventional farms. Cage confinement, added hormones and subtherapeutic antibiotics \
          prohibited. Standards extend to transport and slaughter. Many Certified Humane \
          brands/farms are widely available from larger retailers. Outdoor access not required \
          for birds and pigs. Unless the words “free-range” or “pasture” also appear on the \
          package, assume pork, poultry and egg products come from farms without outdoor access. \
          Feedlots for cows permitted for limited periods, with standards for space, shade and \
          windbreaks that are lacking on conventional feedlots. Standards do not extend to \
          breeding animals, nor do they ensure higher-welfare breeds for animals, including \
          broiler chickens.1 100% compliance verified by auditors on-farm every 12 months, \
          except for Certified Humane “producer groups” and “beef marketing groups,” wherein \
          participating farms conduct a percentage of their own audits. It is not possible to \
          determine which products are from \“producer group\” or \“beef marketing group\” arrangements."
          },
        {title: "ANIMAL WELFARE APPROVED",
          def: "A fully pasture-based animal welfare certification program, available only to \
          smaller, independent family farms. Requires continuous access to pasture or range \
          for all animals. Feedlots, cage confinement, added hormones and subtherapeutic \
          (preventative or growth-promoting) antibiotics prohibited. Standards extend to breeding \
          animals, transport and slaughter. Standards ensure higher-welfare breeds for animals. \
          100% compliance verified by auditors on every farm every 12 months. Focus on small \
          farms makes it difficult for larger retailers to consistently offer AWA-certified products, \
          but they often are found at farmers markets and smaller retailers/co-ops."
          },
      ]
    }
  },
    head() {
    return {
      title: 'Know Your Egg',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Ever wonder what those labels on your egg carton really mean? See explanations of common certifications here, and find out how you can learn more.'
        }
      ]
    }
  }
}
</script>



<style lang="scss">
@import '../assets/css/settings.variables';

#content-link {
  cursor: pointer;
  font-weight: bolder;
  border: none;
  color: $dkgray;
  text-decoration: underline dotted $yellow;
}

</style>
