export default {
  async fetch(request, env, ctx) {
    const url = new URL(request.url);
    url.hostname = 'Your.Domain.netlify.app';
    
    const modifiedRequest = new Request(url, request);
    
    return fetch(modifiedRequest);
  },
};